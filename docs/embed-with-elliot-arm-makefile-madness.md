# 嵌入埃利奥特:ARM Makefile 疯狂

> 原文：<https://hackaday.com/2016/03/22/embed-with-elliot-arm-makefile-madness/>

为了结束我对`make`和 makefile 的快速浏览，我们将看看两个可能用于构建 ARM 项目的 makefile。虽然我特别针对 STM32F407，我桌上的[开发板](http://www.st.com/web/catalog/tools/FM116/SC959/SS1532/PF252419)上的芯片，但将这些扩展到任何 ST ARM 芯片都相当简单，只需多做一点工作就可以扩展到任何 ARM 处理器。

如果您已经阅读了本系列的前两部分，我[展示了`make`](http://hackaday.com/2016/03/11/embed-with-elliot-march-makefile-madness/) 的一些基本用法，它们充分利用了内置规则。然后，我们[将这些规则扩展到 AVR 系列微控制器](http://hackaday.com/2016/03/15/embed-with-elliot-microcontroller-makefiles/)的交叉编译。现在我们要处理一个更复杂的芯片，这意味着要用支持库来编译。虽然不是必需的，但在一些额外的帮助下，让 LED 在 ARM 平台上闪烁要容易得多。

像 Arduino 或 [mbed](https://www.mbed.com/en/) 或类似的 IDE 的主要贡献之一是通过下拉菜单轻松包含外部库。如果您以前从未构建过基于 makefile 的项目，您可能会惊讶于向项目中添加库并不特别困难。


## ARM Makefile Take One:显式版本

首先，我们的 [ARM makefile](https://gist.github.com/hexagon5un/48df2a236531d3ff01af) 很像我们的 AVR 版本。我们需要指定交叉编译工具，以便计算机不会以其本机格式构建文件，并分别使用`CFLAGS`和`LFLAGS`隐式变量传递一些编译和链接器标志。

```

## Cross-compilation commands 
CC      = arm-none-eabi-gcc
AR      = arm-none-eabi-ar
OBJCOPY = arm-none-eabi-objcopy
SIZE    = arm-none-eabi-size
...
## Platform and optimization options
CFLAGS = -c -fno-common -Os -g -mcpu=cortex-m4 -mthumb 
CFLAGS += -Wall -ffunction-sections -fdata-sections -fno-builtin
CFLAGS += -Wno-unused-function -ffreestanding
LFLAGS = -Tstm32f4.ld -nostartfiles -Wl,--gc-sections

```

上一次 AVR makefile 共享了许多这样的选项——例如，将函数分成各自的部分，并对未使用的部分进行垃圾收集。ARM 特定条目包括处理器和“thumb”指令集选项。最后，在链接器标志`LFLAGS`中，我们将一个内存映射(`stm32f4.ld`)传递给链接器，告诉它所有东西都需要放在内存中的什么位置。在 AVR 的情况下，我们不需要这个文件，因为芯片有一个简单和一致的内存布局，GCC 可以为我们填充。在 ARM 世界中并非如此，但是您可以在您正在使用的开发库中为您的项目找到合适的内存映射。

### 规则

构建项目的规则并不特别复杂。因为`make`规则是根据目标和它们的依赖关系来指定的，所以通过规则链向后思考通常是最容易的。在这种情况下，我的 ARM flash 程序员需要一个原始的二进制图像文件发送到芯片，所以我们可以从那里开始。`object-copy`命令从`.elf`文件生成二进制文件，链接器从编译的对象生成`.elf`文件，默认规则将我们的源代码编译成对象。

```

## Rules
all: main.bin size flash

%.bin: %.elf
    $(OBJCOPY) --strip-unneeded -O binary $< $@

main.elf: $(OBJS) stm32f4.ld
    $(LD) $(LFLAGS) -o main.elf $(OBJS)

```

这并不难，是吗？定义的第一个规则总是默认的，当你输入`make`时就会运行，所以我倾向于把它做得更好。在这种情况下，它编译所需的二进制文件，打印出其大小，并将其一次性刷新到芯片中。它就像任何 IDE 中的“什么都做”按钮，只是我不需要把手移到鼠标上点击。(记住`$<`是 makefile——依赖关系的代名词——`.elf`文件——`$@`是包含目标`.bin`的变量。)

### 库:标题

这就把我们带到了图书馆。上面制作`main.elf`的规则依赖于一个我们还没有定义的变量`OBJS`(对象)，这就是我们要包含其他人的代码(OPC)的地方。(是啊，你了解我。)在 C 中，包含其他模块只是将您的代码和 OPC 都编译成目标文件，包括一个头文件来告诉编译器哪些函数来自哪些文件，并将这些对象链接在一起。

在我们的例子中，我们将链接到 F4 处理器的 [CMSIS 标准 ARM 库](http://www.arm.com/products/processors/cortex-m/cortex-microcontroller-software-interface-standard.php)和 [ST 的 HAL 驱动程序库。因为我做过一点 STM32F4 编程，我喜欢把这些库放在中心的某个地方，而不是为每个子项目重复它们，这意味着我必须告诉`make`在哪里找到要包含的头文件和提供函数的原始 C 源文件。](http://www.st.com/web/en/catalog/tools/PF259243)

头文件很简单，所以让我们先处理它们。您只需将`-I[your/directory/here]`选项传递给编译器，它就知道去那里寻找`.h`文件。(确保您还包括当前目录！)

```

## Library headers
CFLAGS += -I./ 
CFLAGS += -I/usr/local/lib/CMSIS/Device/ST/STM32F4xx/Include/
CFLAGS += -I/usr/local/lib/CMSIS/Include/
CFLAGS += -I/usr/local/lib/STM32F4xx_HAL_Driver/Inc/

```

在这种情况下，我们包括所有 ARM 平台共享的整体 CMSIS 头，以及针对我的芯片的特定头。

### 库:对象

一旦编译器知道在哪里可以找到头文件，我们就需要在插件库中编译实际的 C 代码。像以前一样，我们通过告诉`make`我们想要与所讨论的 C 代码相对应的目标文件来做到这一点。我们指定目标，`make`试图满足依赖关系。

```

# our code
OBJS  = main.o
# startup files and anything else
OBJS += handlers.o startup.o

## Library objects
OBJS += /usr/local/lib/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rcc.o
OBJS += /usr/local/lib/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_gpio.o
OBJS += /usr/local/lib/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal.o
OBJS += /usr/local/lib/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_cortex.o
OBJS += /usr/local/lib/CMSIS/Device/ST/STM32F4xx/Source/Templates/system_stm32f4xx.o

```

从第一个 makefile 示例中可以看出，`make`知道如何将`.c`代码编译成`.o`目标文件。因此，通过将变量`OBJ`设置为某个其他目标的依赖项，对应于所列对象的每个源文件都将被自动编译。因为我们已经有了一个规则，将所有的目标文件链接到一个单独的`main.elf`文件中，我们就完成了！

```

## Rules
main.elf: $(OBJS) stm32f4.ld
    $(LD) $(LFLAGS) -o main.elf $(OBJS)

```

### 细节

makefile 文件的其余部分是方便刷新芯片的规则等等。如果你愿意，可以浏览一下，这里有一个关于如何做的有用提示:如果你想知道`make`在想什么，只需键入`make -p`，它列出了所有的规则和一些变量，考虑到当前的 makefile。`make --warn-undefined-variables`也可以帮助发现错别字——如果你键入`OBJ`而不是`OBJS`。

## Fancier ARM Makefile:构建核心库

系统给了你这么多很酷的自动化工具，真的很难知道什么时候该停止。坦白地说，我可能应该坚持使用一个简单的 makefile，像上面这样只有几个活动部分。在 makefile 中的一个地方有一个包含库代码的所有位的明确列表是非常好的。如果你想知道编译和运行程序需要什么额外的东西，你只需要看看`OBJS`的定义。但是有几个`make`的小技巧也许会在你以后的生活中派上用场，我无法抗拒，所以开始吧。

上面的过程也有一个真正的缺陷。它将目标文件编译到与库源文件相同的目录中。例如，当您最终(重新)在使用不同处理器的项目中使用 CMSIS 目录中的代码时，您将拥有为一个芯片编译的与另一个芯片链接的目标文件，除非您首先小心地将它们全部删除。

### 档案

最好在本地编译目标文件，让许多目标文件在代码目录中浮动。昔日的 OCD 程序员讨厌这种混乱，因此[存档文件](http://www.thegeekstuff.com/2010/08/ar-command-examples/)诞生了。归档文件只是一堆塞进一个文件中的目标文件。要构建一个组件，您需要将目标文件传递给一个归档器，然后生成一个`.a`文件，您可以稍后链接到该文件，最终结果就像您链接了所有组件目标文件一样，只需要更少的输入。

所以让我们把所有的 CMSIS 和 HAL 库编译成一个名为`core.a`的大档案。这样，我们将只需要编译这些对象一次，直到我们下载新版本的库，并且我们将几乎不加思考地自由使用库的任何附加部分。(注意，这违背了我的建议，即具体说明我们包括哪些代码。但是太方便了。)

### 通配符

为了构建`core.a`档案，我们需要在几个不同的目录中为每个源文件创建一个目标文件。我们*可以*列出它们，但是有更好的方法。解决方案是使用一个*通配符*来匹配每个`.c`文件名，然后编辑每个文件的名称，将`.c`改为`.o`，给我们一个完整的对象列表。

这里有一个简单的代码片段，它通过将相应的目标文件定义为可执行的`main`程序的依赖项来编译当前目录中的每个`.c`文件。这使得 makefile 变得又快又脏，因为如果您将它放在一个充满代码的目录中，它通常会做您想要做的事情。

```

SRCS   = $(wildcard *.c)
OBJS   = $(SRCS:.c=.o)
CFLAGS = -Wall -I./

main: $(OBJS)
    $(LD) $(LFLAGS) -o main $(OBJS)

```

因此，我们可以通过通配符各种 CMSIS 和 st 库目录来获得我们的目标文件列表:

```

## Locate the main libraries
CMSIS     = /usr/local/lib/CMSIS
HAL       = /usr/local/lib/STM32F4xx_HAL_Driver
HAL_SRC   = $(HAL)/Src
CMSIS_SRC = $(CMSIS)/Device/ST/STM32F4xx/Source/Templates

CORE_OBJ_SRC         = $(wildcard $(HAL_SRC)/*.c)
CORE_OBJ_SRC        += $(wildcard $(CMSIS_SRC)/*.c)

CORE_LIB_OBJS        = $(CORE_OBJ_SRC:.c=.o)
CORE_LOCAL_LIB_OBJS  = $(notdir $(CORE_LIB_OBJS))

```

这为每个源文件创建了一个目标文件列表，它还做了另一个有趣的事情。`notdir`命令从列表中的每个文件中删除前导目录信息。因此，如果我们有一个像`/usr/local/lib/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rcc.o`这样的长文件名，我们现在只有`stm32f4xx_hal_rcc.o`。我们需要这样做，因为我们想把所有的目标文件都放在当前目录中，所以我们必须指定没有完整路径的目标文件。

### VPATH

我们已经为不同库中的每个源文件准备了一个目标文件，但是我们仍然需要一个规则来制作它们。如果所有的 C 代码都在当前目录中，我们就设置好了，因为当`make`看到`stm32f4xx_hal_rcc.o`时，它试图在`stm32f4xx_hal_rcc.c`之外构建它。可悲的是，`stm32f4xx_hal_rcc.c`住在`/usr/local/lib/STM32F4xx_HAL_Driver/Src/`。如果有一种方法告诉`make`在不同的目录中寻找 C 代码，就像我们告诉编译器在不同的包含目录中寻找头文件一样。进入`VPATH`。

```

VPATH = $(HAL_SRC):$(CMSIS_SRC)

```

长话短说，传递给特殊的`VPATH`变量的冒号分隔的目录列表将位于磁盘上任何位置的 OPC 视为当前目录中我们自己的代码。因此，有了所有核心目标文件的本地化版本列表，并且`VPATH`被正确地设置为指向相应的源代码，我们就可以编译所有的目标文件，并将它们全部放入一个归档文件中。

```

core.a: $(CORE_OBJ_SRC)
    $(MAKE) $(CORE_LOCAL_LIB_OBJS)
    $(AR) rcs core.a $(CORE_LOCAL_LIB_OBJS)
    rm -f $(CORE_LOCAL_LIB_OBJS)

```

`$(MAKE)`自动变量只是调用`make`。在这里，我们有效地为所有的目标文件命名为`make stm32f4xx_hal_i2c_ex.o stm32f4xx_hal_dcmi.o stm32f4xx_hal_pcd.o ...`。`AR`行创建了我们的档案(`core.a`)。然后，我们清理掉现在包含在`core.a`中的所有无关的对象文件。干净整洁。

### 魔法:把所有东西放在一起

概括一下:我们使用通配符来标识所有的源代码并获得相应的对象文件名。`VPATH`指向外文库中的源文件，因此`make`可以找到远程源文件。然后，我们创建每个目标文件，并将它们一起放入一个归档文件中，然后进行清理。现在我们准备好根据这个庞大的函数库来编译我们的个人代码。但是不要担心，因为我们通过了`CFLAGS`来删除未使用的代码，所以我们最终只保留了最少的代码。我们再也不用重新编译库代码了。在这个版本的 makefile 中，`OBJS`只是三个本地对象文件。其他的都在`core.a`档案馆。

```

main.elf: $(OBJS) core.a stm32f4.ld
        $(LD) $(LFLAGS) -o main.elf $(OBJS) core.a 

```

这个 makefile 的[核心版本也是完整的，供您阅读。我还将整个项目上传到 GitHub，这样你就可以为 STM32F4 芯片制作它，或者修改它以适用于其他平台。如果人们感兴趣，我将在不久的将来做一些更多的“ARM 入门”类型的主题。](https://gist.github.com/hexagon5un/90c71f9e74e67ae4c883)

我们仅仅触及了`make`的表面，但是我们已经完成了一个复杂的编译，它可以自动拉入外部代码库并将它们预编译到本地档案中。有了`make`你会陷入无限的麻烦，一旦你开始，你将永远不会停止。只要记住尽可能保持事情简单，记住调试首先是写代码的两倍困难——你会想让自己轻松一些。
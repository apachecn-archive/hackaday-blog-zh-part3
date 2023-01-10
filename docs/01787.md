# 嵌入 Elliot:微控制器生成文件

> 原文：<https://hackaday.com/2016/03/15/embed-with-elliot-microcontroller-makefiles/>

上一次在《与埃利奥特共舞》中，我开始庆祝下个月指挥官的 40 岁生日。我们讨论了使用默认规则的[,以及如何用 makefile 中定义的变量](https://hackaday.com/2016/03/11/embed-with-elliot-march-makefile-madness/)来扩充它们。接下来，我将带您浏览一些可用于实际微控制器代码开发的 makefiles。本周，我们将重点讨论一个用于 AVR 平台的版本，稍后，我将介绍一个稍微复杂一些的版本，用于 ARM Cortex micros 的 ST32M 系列。

在这个过程中，我们会学到一些技巧，但是我们的目标是保持 makefiles 最小化，可读性强，易于扩展。一旦您稍微体验了编写自己的 makefiles 的强大功能，您可能就无法停止添加附加功能——用于刷新、检查二进制文件大小、生成程序集清单等的自定义例程。我将把额外的工作留给您，但是您最终会发现您所做的任何事情都可以通过 makefile 自动完成。

## AVR 生成文件

为微控制器编译不像为台式计算机编译那么简单。这是因为你桌面上的编译器被设计成输出与你桌面的 CPU 所说的相同的机器语言。如果你想创建在 AVR(或任何其他平台)上运行的代码，你需要[交叉编译](https://en.wikipedia.org/wiki/Cross_compiler)，这并不像听起来那么令人畏惧。

交叉编译只是意味着使用非默认的编译器、链接器和其他各种工具。上次，我们在 makefile 中用类似于`CC=gcc`的一行指定了我们想要使用的编译器。这里，我们只需要列出让我们为 AVR 平台编译的最小工具集:

```

## Cross-compilation 
CC = avr-gcc 
OBJCOPY = avr-objcopy 

```

接下来，是项目的具体细节。我们将从项目名称和需要创建的目标文件开始。如果你的代码分布在多个`.c`文件中，你将为项目中的每个`.c`文件指定一个目标文件——这就是`make`知道如何编译它们。这里，我们有一些实用函数，我们在不同的项目中使用，这些项目被分解成它们自己的`utility-functions.c`和`utility-functions.h`文件。

```

## Your project 
TARGET = blinkLED 
OBJECTS = blinkLED.o utility-functions.o 

```

然后，因为`avr-gcc`的`delay`和`usart`库被实现为通过预处理器运行的宏，而不是用常规的 C 代码编译的，我们将需要预先定义一些参数，并将这些值传递给预处理器，以便它可以完成它的工作。我们只是告诉代码 CPU 的运行速度，以及我们希望串行外设使用的波特率。

```

## Chip and project-specific global definitions 
MCU = atmega328p 
F_CPU = 8000000UL
BAUD = 9600UL 
CPPFLAGS = -DF_CPU=$(F_CPU) -DBAUD=$(BAUD) -I. 

```

变量`CPPFLAGS`被用于`make`的[隐含规则](http://web.mit.edu/gnu/doc/html/make_10.html#SEC88)之一——特别是将源文件编译成目标文件的规则。现在，在 AVR 代码中使用宏`F_CPU`的地方，例如，它将被指定的(文字)值替换。

说到隐式规则及其变量，让我们覆盖编译器和链接器阶段的一些缺省值来优化 AVR 代码:

```

## Compiler/linker options 
CFLAGS = -Os -g -std=gnu99 -Wall 
CFLAGS += -ffunction-sections -fdata-sections

TARGET_ARCH = -mmcu=$(MCU)

LDFLAGS = -Wl,-Map,$(TARGET).map 
LDFLAGS += -Wl,--gc-sections 

```

当`blinkLED.c`和`CPPFLAGS`一起被编译成`blinkLED.o`时，使用编译器标志`CFLAGS`。第一行设置优化级别，启用调试挂钩，设置我们正在使用的 C 语言，并要求编译器警告我们任何可能的错误。最后两个`CFLAGS`指示编译器跟踪使用了哪些函数和数据段。再加上下面的链接器标志`--gc-sections`(“垃圾收集部分”)，它们让链接器从你的代码中移除所有不用的函数，如果你只是为了使用其中一个函数而包含一个函数库，这会产生巨大的差异。

`TARGET_ARCH`用于将交叉编译目标架构选项传递给编译器和链接器。它用在创建对象文件的隐式规则中，我们也需要显式地使用它。`-Map`链接器选项告诉链接器使用与你的项目同名的内存映射。好消息是`make`有一个为你制作记忆地图的默认规则，所以你可以一直睡到这一部分。

最后，我们已经设置了所有的变量，我们可以到达目标和规则。

```

## Targets and rules
all: flash

flash: $(TARGET).hex
	avrdude -c usbtiny -p $(MCU) -U flash:w:$(TARGET).hex

%.hex: %.elf
	 $(OBJCOPY) -j .text -j .data -O ihex $&lt; $@

%.elf: $(OBJECTS)
	$(CC) $(LDFLAGS) $(TARGET_ARCH) $^ -o $@

clean: 
	rm -f $(TARGET).elf $(TARGET).hex $(TARGET).map

```

作为我们的默认目标`all`，我们将指定一个所谓的“假”目标`flash`。与实际文件不对应的目标被称为假的，但它们非常有用。我们的`flash`目标依赖于我们需要上传到芯片的十六进制文件，并包括一个规则，以`avrdude`命令的形式进行上传。

现在我们只需要十六进制文件。下一个规则是从`.elf`文件生成`.hex`文件的通用规则，这些文件是一种“[可执行和可链接格式](https://en.wikipedia.org/wiki/Executable_and_Linkable_Format)”，包括所有我们编译的函数、数据和一些额外的特定于 AVR 平台的信息。例如，如果我们使用预先加载到芯片 EEPROM 中的数据，这些数据也会包含在`.elf`文件中。`$<`是一个`make`特殊变量，它指的是一个单独的依赖项，在我们的例子中是有问题的`.elf`文件。`$@`是规则目标的自动变量——在这里，它解析为正在生成的文件的名称。

最后，我们指导`make`如何通过链接我们指定的各种编译后的目标文件来创建一个`.elf`文件。`.elf`文件本质上是一个将所有目标文件组合在一起的地方，从中删除不用的函数。(注意，这是执行垃圾收集的`LDFLAGS`出现的地方。)`$^`是一个特殊的`make`变量，它引用所列出的所有依赖项的*，因此该命令将它们全部链接在一起。*

看起来好像少了点什么。我们从来没有明确地告诉`make`将`.c`代码文件编译成`.o`目标文件！但是`make`已经知道如何做到这一点，我们已经告诉它使用特定于 AVR 的编译器和相关选项，所以没有必要重新编写规则。并且`make`知道它需要构建哪些目标文件，因为我们通过`OBJECTS`变量将它们指定为`.elf`文件的依赖项。

## 扩展和其他花哨的东西

正如这里所介绍的，[这个基本的 AVR makefile](http://ix.io/seE) 将获取您的代码，编译它，链接它，并将其转换为上传者需要直接写入 AVR 闪存的格式。(它甚至做到了这一点！)当然，还有许多其他你可能喜欢做的事情。

例如，您可能想要反汇编代码并检查某些子例程的计时。或者，您可能需要将 EEPROM 的内容从`.elf`文件中取出，这样您就可以将它们预加载到芯片中。AVR 有各种需要设置的保险丝，你的马厩里可能有几个不同的芯片编程器。只要多写几条规则，所有这些和更多的都可以很容易地适应。如果你对一个更全面的 AVR 例子感兴趣，[你可以仔细阅读这个 makefile](https://github.com/hexagon5un/AVR-Programming/blob/master/Chapter02_Programming-AVRs/blinkLED/Makefile) ，我实际上在我的大多数项目中使用它。

但是这里展示的基本思想是如何使用 makefiles 为微控制器平台进行交叉编译的核心。您需要重新定义所有的编译和链接程序以适应您的目标，使用隐式变量定义特定于目标的编译器和链接器选项，然后可能像我们在这里所做的那样编写一些您自己的规则来将它们联系在一起。

如果您对可用于 STM32 ARM 芯片的 makefile 感兴趣，请继续关注下一期的 Embed with Elliot，我们将在其中介绍一个更复杂的编译过程。在这个过程中，我将演示一些更有用的 makefile 技巧，我相信即使您没有使用 ARM 芯片，您也会喜欢这些技巧。三月是 makefile 疯狂！
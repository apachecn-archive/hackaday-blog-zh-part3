# Linux Fu:Make 的强大力量

> 原文：<https://hackaday.com/2018/06/22/linux-fu-the-great-power-of-make/>

多年来，Linux(嗯，通常称为 Linux 的操作系统，是 Linux 内核和 GNU 工具)已经变得比它的 Unix 根源复杂得多。当然，这是不可避免的。然而，这意味着老用户需要慢慢适应新功能，而新用户必须一口气学会所有功能。一个很好的例子就是软件通常是如何在 Linux 系统上构建的。从根本上说，大多数项目使用`make`——一个试图智能运行编译的程序。当连接到非常慢的磁盘驱动器的 100 MHz CPU 需要一天时间来构建一个重要的软件时，这一点尤其重要。从表面上看，make 非常简单。但是今天，看一个典型的 makefile 会让你头疼，许多项目使用了 make 之上的抽象，这进一步混淆了事物。

在本文中，我想向您展示 makefile 有多简单。如果你能构建一个简单的 makefile，你会发现它们比你想象的有更多的用途。我会把重点放在 C 上，因为这是最小公分母。make 文件可以在 shell 提示符下构建任何东西。

## No IDE?

您可能会嘲笑并说您不需要 makefile。IDE 会为您构建软件。这可能是真的，但是许多 ide 实际上都在幕后使用 makefiles。即使是不常导出 makefile 的 ide。这允许您更容易地编写构建脚本或与通常需要 makefile 的连续发布工具集成。

一个例外是 Java。Java 有自己的一套人们使用的构建工具，所以 make 并不常见。然而，当然可以将它与命令行工具一起使用，如`javac`或`gcj`。

## 最简单的生成文件

[![](img/f9f7695085dc4bb7bbf5cc162b925ac3.png)](https://hackaday.com/wp-content/uploads/2018/05/tux1.png) 下面是一个简单的 makefile:

```
hello: hello.c
```

就是这样。真的。这是一个规则，说明有一个名为 hello 的文件，它依赖于 hello.c 文件，如果 hello.c 比 hello 新，则构建 hello。等等，什么？它怎么知道该做什么？通常，您将添加关于如何从其依赖项构建目标(hello)的指令。但是，有默认规则。

如果您在一个目录中创建一个名为 Makefile 的文件以及 [hello.c](https://gist.github.com/szczys/3af48cdb165094945badc92de4c9d897) ,然后在该目录中发出`make`命令，您将看到该命令运行如下:

```
cc hello.c -o hello
```

这很好，因为大多数发行版都有指向默认 C 编译器的 cc。如果你再次运行 make，你会发现它没有构建任何东西。相反，它会报告类似这样的内容:

```
make: 'hello' is up to date.
```

要重新构建它，您需要对 hello.c 进行更改，在 hello.c 上使用 touch 命令，或者删除 hello。顺便说一下，`-n`命令行选项会告诉 make 告诉你它会做什么，而不是实际去做。当您试图弄清楚一个特定的 makefile 在做什么时，这很方便。

如果您愿意，可以使用变量自定义默认值。变量可以来自命令行、环境，也可以在 makefile 中设置。例如:

```
CC=gcc
CFLAGS=-g
hello : hello.c
```

现在您将得到一个类似于以下的命令:

```
gcc -g hello.c -o hello
```

在一个复杂的 makefile 中，您可能想要向已经有的选项中添加选项，您也可以这样做(数字符号#是一个注释):

```
CC=gcc
CFLAGS=-g
# Comment next line to turn off optimization
CFLAGS+=-O
hello : hello.c
```

事实上，正在使用的隐含规则是:

```
$(CC) $(CFLAGS) $(CPPFLAGS) hello.c -o hello
```

注意，按照惯例，变量总是使用`$()`语法。实际上，如果您有一个单字符变量名，您可以省略它(例如，`$X`)，但是这可能不可移植，所以最好的办法是始终使用括号。

## 自定义规则

也许你不想使用默认规则。那没问题。不过，make 程序对文件格式有点执着。如果您以制表符(不仅仅是几个空格；一个真正的选项卡)，那么该行(连同其他行)将像脚本一样运行，而不是默认规则。因此，虽然这不是很优雅，但这是编写 makefile 的一个非常好的方法:

```
hello : hello.c
    gcc -g -O hello.c
```

事实上，您应该使用变量来使您的规则更灵活，就像默认规则一样。您也可以使用通配符。考虑一下这个:

```
% : %.c
    $(CC) $(CPPFLAGS) $(CFLAGS) $< -o $@
```

这或多或少与默认规则相同。百分号匹配任何内容，`$<`获取第一个(在本例中是唯一的)先决条件的名称，即 hello.c，`$@`变量为您提供目标的名称(本例中为 hello)。有更多的变量可用，但这些将让你开始。

您可以有多个脚本行(由默认的系统 shell 处理，尽管您可以更改),只要它们都以制表符开始。还可以添加更多的先决条件。例如:

```
hello : hello.c hello.h mylocallib.h
```

不过，维护起来很繁琐。对于 C 和 C++，大部分编译器(包括 gcc)都有办法创建。d 文件可以自动告诉 make 一个对象依赖什么文件。这超出了本文的范围，但是如果您想了解更多，可以查看 gcc 的`-MMD`选项。

## 我反对

通常，在一个重要的项目中，你不会仅仅编译 C 文件(或者你有的任何东西)。您将把源文件编译成目标文件，然后在最后链接目标文件。默认规则理解这一点，当然，您可以编写自己的规则:

```
hello : hello.o mylib.o
hello.o : hello.c hello.h mylib.h
mylib.o : mylib.c mylib.h
```

感谢默认规则，这就是你所需要的。make 程序足够聪明，可以看到它需要 hello.o，它会去寻找 hello.o 的规则等等。当然，如果您想控制构建过程中发生的事情，您可以在这些脚本行之后添加一个或多个脚本行。

默认情况下，make 只尝试构建它找到的第一个东西。有时你会首先看到一个假目标，就像这样:

```
all : hello libtest config-editor
```

那么，假设你在别处有这三个程序的规则，make 将构建所有这三个程序。只要工作目录中没有文件名“all ”,这种方法就有效。为了防止出现这种问题，您可以在 makefile 中使用以下语句将该目标声明为假的:

```
.PHONY: all
```

您也可以将动作附加到虚假的目标上。例如，您经常会看到这样的内容:

```
.PHONY: clean
clean: 
     rm *.o
```

然后，您可以从命令行发出`make clean`来删除所有的目标文件。你可能不会把它作为第一个目标，或者把它添加到类似 all 的东西中。另一个常见的做法是创建一个虚假的目标，可以将您的代码刻录到微控制器上，这样您就可以发出类似“make program”的命令，将代码下载到芯片上。

## 愚蠢的恶作剧

[![](img/b9355155f8f564c09d182e0892e92a02.png)](https://hackaday.com/wp-content/uploads/2018/05/tux2.png) 通常，你用 make 来构建软件。但是像任何其他 Unix/Linux 工具一样，您会发现人们使用它做各种各样的事情。例如，很容易构建一个 makefile，它使用 [pandoc](https://hackaday.com/2017/05/23/stupid-git-tricks/) 在文档发生变化时将其转换为多种格式。

关键是要意识到 make 将构建一个依赖树，找出需要注意的部分，并运行这些部分的脚本。脚本不一定是构建步骤。他们可以复制文件(甚至远程使用 scp 之类的东西)，删除文件，或者做任何 Linux shell 脚本可以做的事情。

## 但是等等，还有更多

关于 make 还有很多东西要学，但是根据你已经知道的，你可以做很多事情。你可以阅读[手册](https://www.gnu.org/software/make/manual/make.html)，当然要了解更多。如果你看一个重要的 makefile，比如为 [Arduino 项目](https://hackaday.com/2015/10/01/arduino-development-theres-a-makefile-for-that/)做的 makefile，你会发现有很多东西我们没有谈到。但是你仍然可以从中挑选出很多。

下一次，我将讨论一些采用不同输入格式并生成 makefile 的方案。人们想这么做有几个原因。一个是抽象软件可能会确定依赖关系或对生成的 makefile 进行其他更改。此外，这些工具中的大多数可以为不同的平台生成构建脚本。举个例子，如果你看过`automake`或者`cmake`，这些就是我所说的工具。

然而，你不需要像我们在 Raspberry Pi 或其他嵌入式系统上经常做的那样，为许多小项目准备任何花哨的东西。基本的 make 功能将带你走很长的路。尤其是对于以具有少量文件和依赖项的单一类型计算机为目标的项目。
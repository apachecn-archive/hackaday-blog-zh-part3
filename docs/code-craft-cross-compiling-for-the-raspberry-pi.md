# 代码工艺:树莓派的交叉编译

> 原文：<https://hackaday.com/2016/02/03/code-craft-cross-compiling-for-the-raspberry-pi/>

有时候，没有什么地方比得上你的桌面。您已经设置或安装了您最喜欢的开发工具和参考资料，当您试图在一个不熟悉的或简单的非定制系统上工作时，这是一件痛苦的事情。在你的桌面上，一切触手可及。如果你想在网上搜索，浏览器就在 alt-tab 键附近。如果你需要一个计算器，它就在那里运行。您的编辑器已经用您喜欢的颜色突出显示了语法。

当在 Raspberry Pi 上开发时，除非您花时间按照自己的喜好配置 Pi，否则您会将所有这些舒适的环境抛在脑后。然后，当你安装一个新的发行版时，所有这些都会被删除，就像最近从 Wheezy 到 Jessie 的变化一样。即使这样，在桌面和 Pi 之间来回切换也是令人沮丧的，因为在另一个系统上总有你需要的东西。我通常的评论是，“脏话”，字面意思。

在你的桌面上交叉开发是一个非常可行的解决方案。我们将通过设置您的桌面和 Pi 来完成此任务。这意味着在您的桌面上加载一个 Pi ARM 工具链，并在 Pi 上加载一个调试服务器。这将让您在舒适的桌面上进行开发和调试。一个额外的好处是，当你把 Pi 放在一个机器人里，你可以通过无线链接进行调试。

# 跨系统开发

![Rud's SRR Rover Trying to Dig Under Block](img/f116f646db965bcd0b858db191aa1af6.png)

Rud’s SRR Rover Trying to Dig Under Block

交叉开发实际上相当普遍。如果你已经在你的桌面上编译了 Arduino，你就已经完成了。在 80 年代后期，我使用基于 80×86 的 pc 机为使用 80286 处理器的 STD 总线系统开发软件。最近，为了参加 2013 年 NASA 样品回收机器人竞赛，我调试了我的漫游者，通过 WiFi 在 ITX 的个人电脑上运行 XP。

交叉开发是 Pi 非常自然的方法，因为这是 Raspian 的构建方式。我一直想尝试这一点，在第一次通过 Pi 激光雷达项目后，决定现在是时候了。

## 设置交叉构建工具

我的台式机用的是 Ubuntu 14.04，笔记本用的是 15.04。我首先为交叉开发设置桌面，然后在笔记本上重复这些步骤来验证这个过程。这个过程在 Linux 上应该没问题，在 Windows 下也可以做类似的事情。如果您使用早期的发行版，请小心，因为 ARM 开发库可能不是 Pi 上使用的库。

第一步是在桌面或主机系统上安装开发工具。从命令行运行以下命令:

```
sudo apt-get install build-essential
sudo apt-get install g++-arm-linux-gnueabihf
sudo apt-get install gdb-multiarch

```

第一行安装通用构建工具。第二个为 Pi 的 ARM 处理器安装 C 和 C++编译器和构建工具。第三个安装了一个版本的 *gdb* 调试工具，它可以与目标系统一起工作，而不考虑处理器架构。在某处记下 arm 架构名称， *arm-linux-gnueabihf-* ，因为它被用作区分 ARM 工具和主机系统工具的前缀。请确保字符串末尾有破折号。

要测试一切是否正常，请输入下面一行，它应该报告所安装的 G++编译器的版本，以及许多其他信息:

```
arm-linux-gnueabihf-g++ -v
```

如果出现错误，请返回到构建工具的安装过程。

## 你好，来自 Pi 的世界！！！

您的主机系统现在应该可以构建一个 Raspberry Pi 程序了。让我们从无处不在的 *Hello World* 开始，当然是用 C++语言。创建一个文件 *hello.cpp* 并输入源代码:

```

#include &lt;iostream&gt;
using namespace std;

int main() {
	cout &lt;&lt; &quot;!!!Hello World From Pi!!!&quot; &lt;&lt; endl;
	return 0;
}

```

要构建该程序，请运行以下两个命令行:

```
arm-linux-gnueabihf-g++ -O3 -g3 -Wall -c -o -fPIC "hello.o" "hello.cpp"
arm-linux-gnueabihf-g++ -o "hello" hello.o

```

第一行编译文件 *hello.cpp* ，第二行链接编译器输出以构建可执行文件 *hello* 。假设一切顺利，输入以下命令，您应该会看到类似于斜体显示的输出:

```
file hello
*hello: ELF 32-bit LSB executable, ARM, EABI5 version 1 (SYSV), 
dynamically linked (uses shared libs), for GNU/Linux 2.6.32, 
BuildID[sha1]=bc5e0850c0dc9d88ba60887facf52c00222dc746, not stripped*
```

这告诉我们，该文件是为 ARM 处理器而不是为您的主机系统构建的。将该文件复制到您 Pi 中，设置 execute 和 owner 权限位，执行它，它将生成“Hello World”消息。现在，您已经准备好为 Pi 进行交叉编译了。

虽然这很好，但是缺少在目标 Pi 上调试软件的能力。通过用输出语句或日志跟踪执行可以做很多事情，但是没有什么比通过一个拒绝工作的讨厌的例程更好了。

## 跨系统调试

使用程序 *gdb* 对 GCC 工具集进行调试。我们安装的最后一个项目， *gdb-multiarch* ，在主机系统上提供调试功能。现在我们需要在 Pi 目标系统上安装一个调试服务器，我们可以从桌面连接到它，并控制目标系统上的执行。切换到 Pi 并运行下面的安装来获得目标版本的 *gdb* :

```
sudo apt-get install gdbserver

```

注意，当 *gdbserver* 运行时，它在 Pi 上创建了一个大的安全漏洞。这不太可能被利用，因为您是在本地网络上运行，但是不要设置为在启动时运行，然后在野外部署系统。

现在确定您想要将可执行文件放在 Pi 的什么位置。我创建了一个目录 *remote* ，您将在示例中看到。要运行服务器，我们将只使用这个简单的命令行，如下所示，但您应该探索一些选项:

```
gdbserver --multi mysticlakelinux:2001
```

这个命令启动服务器，并告诉它连续运行。计算机名或 IP 地址是主机的名称。在我的情况下，它是 *mysticlakelinux* 。最后，2001 是主机和目标将用于通信的端口。一定要记住它，因为在主机上调试时需要它。

我们现在已经完成了 Pi，但是让 SSH 终端继续运行。除了保持服务器运行之外，它还会显示错误信息，当最终一切正常时，还会显示程序的输出。现在切换回主机，打开终端，切换到“Hello World”程序的目录，这样我们就可以开始调试了。

程序 *gdb-multiarch* 是一个交互式程序。有许多可以输入的命令。它还需要大量的命令行选项，包括从文本文件中读取交互式命令的能力。我们将做足够的工作来演示它运行程序，因为有太多的选项和功能。

在主机上，输入命令:

```
gdb-multiarch
```

您应该得到一串输出，后面跟着提示 *(gdb)* 。将来你可能想在命令行中添加选项 *-q* 。这扼杀了介绍性信息。在提示符下，使用您的 Pi 的名称，输入以下命令，您应该会看到响应，如这里的斜体所示:

```
target extended-remote pizero.local:2001
*Remote debugging using pizero.local:2001*
set remote exec-file remote/hello
*[[no response]]*
file hello
*Reading symbols from hello...done.*
```

*目标*命令告诉 *gdb* 要使用的目标系统名称 *pizero* 和端口 *2001* 。如果成功了，您将得到所示的响应；否则会出现超时消息。 *set remote* 行指定要在 Pi 目标系统上使用的文件位置。请记住，每次更改可执行文件时，都需要将其复制到目标系统上。我们将在下面看到如何在 gdb 中实现这一点。最后一个命令， *file* ，是主机上的路径和文件名。这可以是调试器运行的目录以外的目录。现在，键入以下内容并获得如下所示的响应:

```
run
*Starting program: /home/rmerriam/development/ws/pi/hello/Debug/hello*
*[[ a bunch more lines, some warnings and stuff to ignore for now ]]*
*[Inferior 1 (process 1532) exited normally]*
```

如果成功了，你会看到最后一行。现在切换到连接到 Pi 的 SSH 终端，您将看到几行状态信息、程序的输出、一个空行和一个报告程序退出状态的行。如果这些都不起作用，请检查来自服务器的错误消息。它应该解释正在发生的事情。通常你告诉 gdb 的内容和可执行文件的位置不匹配。

调试器提供了大量用于操作断点、继续执行、列出程序等的命令。例如，输入 *main* ，当到达 *main()* 时，程序停止。“c”在断点后运行程序。为了帮助调试，有一个有趣的模式，终端用户界面，或 *tui* 。您可以通过键入 Ctrl-x、Ctrl-a 来访问和离开它。这种模式提供了显示源代码、寄存器、汇编语言和其他信息的窗口。

gdb 的一个不幸的方面是它不会自动复制可执行文件的新版本，至少我没有发现。这可以通过在 *gdb* 中输入一个‘转义’命令来处理，这是一个运行在主机上但在调试器之外的普通 Linux 命令。 *scp* 命令将文件从一个系统复制到另一个系统。以下是我的尝试和回应:

```
!scp hello pi@pizero.local:/home/pi/remote/hello
*pi@pizero.local's password:* 
*hello                  100% 69KB 68.7KB/s 00:00* 
```

这并不坏，除了它每次都要求输入密码。解决方法是像这样使用 *sshpass* :

```
!sshpass -p 'password' scp hello pi@pizero.local:/home/pi/remote/hello
```

一旦你启动 *gdb* 并设置好一切，你就不需要重新输入所有的设置命令了。一个解决方案是将它们全部添加到一个文本文件中，并使用 *source* 命令在 *gdb* 中运行它们。另一个选择是永远不离开 *gdb* 。键入“！”在行首将命令传递给 shell 来运行并返回。键入“！”你在主机系统命令行。您可以在终端环境中工作，直到准备好返回调试。就像任何其他终端一样，键入 *exit* ，您将回到 *gdb* 中。

# 包裹

如果您喜欢使用命令行进行调试，那么您将需要探索使用 *gdb* 的细节。您可以设置断点，逐句通过程序，并显示有关程序的信息。我过去在嵌入式系统工作中使用过类似的命令行工具。不用了，谢谢，我将继续使用 Eclipse，在下一篇文章中，我将介绍这个过程。那篇文章还将重新讨论激光雷达项目和另一个 Pi 库， *pigpio* 。到时候见！
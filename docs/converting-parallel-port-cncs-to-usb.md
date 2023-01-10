# 将并行端口 CNCs 转换为 USB

> 原文：<https://hackaday.com/2017/05/05/converting-parallel-port-cncs-to-usb/>

如果你正在寻找一个小型的台式数控机床，用于印刷电路板和轻型铣削，无处不在的 Sherline 数控机床是一个不错的选择。不过，这有一个问题:通常，Sherline CNC 控制器通过并行端口运行。虽然我们中的一些人仍然有一个 Windows 98 的战斗站，但[大卫]没有。相反，他制作了一个 USB 加密狗，并编写了软件，将这个迷你 CNC 变成可与现代计算机一起使用的东西。

首先，硬件。该构建的核心是基于 PIC18F2455 微控制器的 rt-stepper 加密狗。该芯片用最少的部件将 USB 转换成并行端口，以进行实时控制。它的速度很快——至少和我们现在使用的古代笔记本电脑中的并行端口一样快，并且直接插入 Sherline 的 CNC 控制器盒中。

软件才是真正的亮点。[用来控制这个加密狗的应用程序](http://ecklersoft.com/pymini.html)是 EMC/LinuxCNC 项目的一个黑客，用漂亮的可移植 Python 编写。该应用程序产生步进脉冲，但时序由加密狗维持；不需要实时内核。

有很多选择有一个桌面数控机床为路由覆铜板，木材，黄铜，铝。其他工厂很棒，发明家 X-Carve 和 T2-Carvey 可以胜任这项任务。尽管如此，对于一些小而相对便宜的东西来说，Sherline 还是很受欢迎的，有了这个小加密狗，你实际上可以在现代计算机上使用它。查看下面的演示视频。

 [https://www.youtube.com/embed/vXCyXvo4SUg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vXCyXvo4SUg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


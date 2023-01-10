# 带有自定义语言的 6502

> 原文：<https://hackaday.com/2018/02/13/a-6502-with-a-custom-langauge/>

6502 与黑客有着悠久的历史。苹果电脑(没有键盘甚至没有外壳的那种)有一个 6502。金正日 1 号也是。虽然[Dolo 的]版本[更精致一点](https://hackaday.io/project/5789-6502-homebrew-computer)。几年前，他在回应我们的一次竞赛时开始了这项工作，但从那以后，他一直在对它进行改进。特别是，自定义编程语言 Dflat 最近有了许多改进，包括真正的函数和高分辨率绘图。

硬件具有运行在 2.5 MHz 以上的 CPU、44K 的 RAM、16K 的 PROM 和 16K 的视频 RAM。有大量的 I/O，包括键盘、声音和操纵杆。一个 SD 卡提供大容量存储，所有这些都放在一个被黑客入侵的 BBC 微型盒子里。你可以在下面看到一个概述视频。

硬件安装在试验板上，对于这种规模的电路来说，这总是很困难的。然而，其中真正有趣的部分是类似于 Basic 的结构化语言，称为 Dflat。据我们所知，这与上世纪 90 年代阿尔·史蒂文的降 D 调语言毫无关系。该 Dflat 具有驱动 6502 视频、声音和其他 I/O 的功能。

该语言处理整数和字符串，尽管有行号可供编辑，但它们不被用作控制目标。它还支持一维字符串数组和二维整数数组。

这将是大铁早在一天，试验板建设是整齐地完成。如果你更喜欢 Z80，[你也可以试装那个](https://hackaday.com/2017/01/02/retrocomputing-for-4-with-a-z80/)。如果你想要更多的电路板，[总有这个](https://hackaday.com/2017/04/10/8-bit-breadboard-computer-is-up-to-8-hours/)。

 [https://www.youtube.com/embed/UaU-4s60Qm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UaU-4s60Qm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


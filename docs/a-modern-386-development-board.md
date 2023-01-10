# 现代 386 开发板

> 原文：<https://hackaday.com/2015/11/17/a-modern-386-development-board/>

有些读者可能对他们的第一台基于 386 的个人电脑、调制解调器的哔哔声和嘶嘶声以及软盘驱动器步进电机的经典声音怀有怀旧之情。也许那个我们永远也搞不清楚的涡轮按钮。

如果你今天想要 386 处理器的能力，你很幸运:[Pierre Surply]为 80386 sx CPU 开发了一种现代的[开发板。该板基于 LQFP 封装的 386 处理器和 Altera Cyclone IV FPGA，便于焊接。](http://blog.lse.epita.fr/articles/77-lsepc-intro.html)

为了让 CPU 运行，FPGA 模拟了你通常在 PC 主板上看到的芯片组。FPGA 充当 CPU 的总线控制器和存储器控制器。在板上，FPGA 上有一个 SRAM 芯片和内部存储器，可以通过 386 的总线访问协议进行访问。

FPGA 还提供调试功能。运行在 FPGA 上的监控应用通过 FTDI USB 向 UART 芯片提供调试功能。这使您可以从 PC 上控制 CPU 的操作，以便进行调试。FPGA 的存储器可以通过 JTAG 接口进行编程。

该项目是非常好的记录，是一个伟大的阅读，如果你想知道你的老 386 实际上是如何工作的。它甚至可以手工焊接，所以喜欢冒险的人可以拿起设计文件试一试。法语读者也可以观看下面的视频。

 [https://www.youtube.com/embed/v4jbp585eFA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/v4jbp585eFA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


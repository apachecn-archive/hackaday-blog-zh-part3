# 多功能树莓 Pi 芯片播放器

> 原文：<https://hackaday.com/2017/06/11/multifunction-raspberry-pi-chiptune-player/>

通用仪器的 AY-3-8910 是一种与视频游戏音乐相关的芯片，在街机游戏和弹球机中很受欢迎。这种 IC 产生的芯片曲调是标志性的，让人想起一个伟大的电子时代。[Deater]通过他的 [Raspberry Pi AY-3-8910 项目](http://www.deater.net/weave/vmwprod/hardware/ay-3-8910/)在创造新老和谐方面做了令人惊叹的工作。

[Deater]已经在试验板上向我们展示了该项目的早期版本,然而在制作了一些 PCB 和外壳之后，结果更加令人印象深刻。该系统由两个而非一个 AY-3-8910 立体声系统组成，通过 MAX98306 分线点进行放大。Raspberry Pi 2 通过 SPI 驱动的 74HC595 移位寄存器发送 6 个通道的数据。从矩阵到条形图，甚至 14 段显示器都有剩余。整个 PCB 被视为一顶帽子，由位于 DS1307 RTC 分线板旁边的 EEPROM 提供。附件很简单，但在展示内部结构和 PCB 艺术方面非常有效。

[Deater]提供的软件将该项目的功能扩展到 chiptunes 播放器之外。有一个程序可以将这些设备用作闹钟、CPU 计量器、电子琴，甚至是俄罗斯方块的可玩版本，如下面的演示视频所示。这篇博文信息量很大，以时间顺序展示了设计在不同发展阶段的进展。[Deater]提供了一整套说明以及原理图和发布在 [GitHub](https://github.com/deater/vmw-meter.git) 上的代码。

如果你对 Arduino 情有独钟，你可能会想看看 8 位版本的芯片调谐播放器，如果你渴望一些旧的硬件外设信息，一定要看看铁幕时期的电脑珍品 T2。

 [https://www.youtube.com/embed/kB-iyDEXOrY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kB-iyDEXOrY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


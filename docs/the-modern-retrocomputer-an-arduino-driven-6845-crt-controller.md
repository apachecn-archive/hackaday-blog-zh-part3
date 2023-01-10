# 现代反计算机:Arduino 驱动的 6845 CRT 控制器

> 原文：<https://hackaday.com/2017/05/14/the-modern-retrocomputer-an-arduino-driven-6845-crt-controller/>

[MmmmFloorPie]恢复了一个旧项目，创建了一个 [6845 CRT 控制器和一个现代 Arduino Uno](http://imgur.com/a/DEcdK) 的复古混搭。说到芯片，摩托罗拉 6845 是阴极射线管(CRT)接口的鼻祖。它被用在 IBM 单色显示适配器、Hercules 图形控制器、CGA、Apple II 终端卡以及许多其他微型计算机和终端系统中。

早在 1989 年，[MmmmFloorPie]是一名大学四年级学生。他的顶点项目是一台基于 68000 的计算机，它可以记录和回放音频，也可以在 CRT 上显示波形。有问题的阴极射线管是从《大众科学》杂志的分类目录中订购的。这是一个裸管，所以它装运的重纸箱被重新用作箱子。

快进到今天，[MmmmFloorPie]想要启动他的旧项目。68000 板死了，他无法调试数百个点对点的焊接连接。CRT 接口是一块独立的板，包括 6845 和 32k 字节的 RAM。只需要一点黑客技术就能实现。但是什么会取代微处理器呢？

[MmmmFloorPie]决定用 Arduino Uno 来咬一口 68000 总线。Uno 没有足够的 I/O 引脚来驱动完整的地址数据总线，因此使用 74LS574 三态触发器来锁存地址数据。可以想象，整个系统比运行真正的 68000 要慢得多。当限制他的视频 RAM 写入垂直回扫周期时，这篇文章顶部显示的屏幕花了整整 40 秒才显示出来。对于任何实际应用来说太慢了，但足以证明该系统是有效的。我们希望[MmmmFloorPie]受到启发，让他的经典家酿计算机的其余部分起死回生！

Reddit 上有更多关于这次黑客攻击的信息。对经典视频控制器感兴趣？查看[这篇关于 VGA](http://hackaday.com/2016/01/29/vga-in-memoriam/) 死亡的帖子，或者学习如何用 Arduino 在 LCD 上制作 [3D 图形。](http://hackaday.com/2016/01/02/better-3d-graphics-on-the-arduino/)
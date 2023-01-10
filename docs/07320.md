# Commodore 64 的反向调制解调器

> 原文：<https://hackaday.com/2017/10/07/retromodem-for-the-commodore-64/>

复古计算机很有趣，但与现代硬件相比，它的能力终究有限。纠正这种情况的一种流行做法是将早期的家用电脑连接到互联网上。为此，[que]为准将 64 建造了一个反向调制解调器。

构建从英特尔 14.4 调制解调器的案例开始。对于准将 64 时代来说有点快，但如果处理得有品味，时代错误是迷人的。内部是一个带有以太网模块的 Arduino，用于处理向外部世界运送数据包的繁重工作。[que]花时间为适当的复古外观连接状态 led，这确实为项目增添了一些东西。它们打开和关闭以指示调制解调器上的各种设置——当波特率更改为更高速度时，在下面的视频中看到“HS”LED 灯亮起非常好。

该项目实现了大部分的 Hayes 命令集，所以你可以通过一个串行终端与它交互，就像 1983 年一样。[que]并没有详细说明如何将它们组合在一起，但是对于有经验的代码战士来说，这是一个可以在一两个周末内完成的项目。更现代的说法是，也许你想通过无线网络连接你的 C64？

 [https://www.youtube.com/embed/DIJ1nv-vFDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DIJ1nv-vFDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


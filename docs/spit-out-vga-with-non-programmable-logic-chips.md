# 用不可编程逻辑芯片吐出 VGA

> 原文：<https://hackaday.com/2015/10/15/spit-out-vga-with-non-programmable-logic-chips/>

紧要关头用微控制器修改协议并不少见。I2C 经常从零开始，简单的串行协议也是如此，偶尔复杂的系统如以太网，以及一大堆其他通信标准也是如此。但由于时序要求，VGA 变得相当棘手，所以它在 bitbang 中不太常见。[斯文]完全抛开了谨慎。他不只是在 Arduino 上 bitbang VGA，而是更进一步，[配置了 7400 个逻辑芯片的阵列来输出 VGA 信号](http://www.skrasser.com/blog/2015/09/05/vga-from-scratch/)。

[Sven]的项目分为两部分。在第一部分中，他讨论了选择分辨率和设置定时信号。他继续输出一个简单的 VGA 信号，这个信号可以用一个门显示在显示器上。在这一点上，只有一个红色的图像显示，但从监视器获得信号锁定是一个很好的概念证明，并[斯文]移动到更复杂的显示技巧。

在项目的下一次迭代中，[Sven] [谈到添加更多的电路](http://www.skrasser.com/blog/2015/10/08/vga-from-scratch-part-2/)来处理像帧计数、几何和颜色这样的事情。显示的图形首先在模拟器中规划出来，然后用于为特定的图形显示设计 7400 芯片配置。让我们窃笑的是，[斯文]报告说他的显示器设法在这个最新的项目中幸存下来！

我们不记得以前见过不可编程集成电路用于 VGA 一代。但是在 Arduino 或 SD 卡插槽中对信号[进行位碰撞是对你在嵌入式系统中计算和实现精确计时能力的一个巨大考验。试试看！](http://hackaday.com/2014/06/10/640x480-vga-on-an-arduino/)

 [https://www.youtube.com/embed/gSAkuj3EI_w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gSAkuj3EI_w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


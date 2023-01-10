# 用 555 定时器消除机床颤振

> 原文：<https://hackaday.com/2017/10/06/fighting-machine-tool-chatter-with-a-555-timer/>

振动是几乎所有机械加工操作中的一个现实。无论是铣削、钻孔、车削还是磨削，振动都会导致颤振，从而损坏零件。打击颤振通常是增加机器质量的问题，但如果你聪明，也可以通过电子方式减少颤振。(YouTube，下面嵌入。)

当你对共振有所了解时，机器振动和颤动就开始有意义了。[AvE]在视频中花了相当多的时间解释和演示共鸣——这是对他惯用的咸味商店语言的合理警告。他的演示目标是表明颤振来自于柔性梁的持续激励，在这种情况下，柔性梁是没有尾座支撑的车床卡盘中的一部分。这个想法是通过稍微快速改变车床的速度，系统不会在共振频率上花费很长时间。他的方法依赖于带有可编程 IO 引脚的变频驱动器(VFD)。一个简单的 555 定时器板驱动一个继电器来开关 IO 引脚，使 VFD 上下循环几赫兹。随着定时器的循环，主轴转速变化 100 RPM，减少了在共振频率下花费的时间。结果看起来并不太糟——不完美，但确实有所改善。

这是一个值得记住的有趣技术，比通常的技术[更大的质量](http://hackaday.com/2017/03/05/bulking-up-a-lightweight-lathe-with-a-concrete-cart/)有了很大的进步。

 [https://www.youtube.com/embed/po5VUW3I8P8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/po5VUW3I8P8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


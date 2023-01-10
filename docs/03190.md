# 蓝牙 HID 游戏手柄和 HC-05 串行破解

> 原文：<https://hackaday.com/2016/08/10/bluetooth-hid-gamepad-and-hc-05-serial-hack/>

"先有鸡还是先有蛋？"不要用愚蠢的问题来打扰我们，它们都共同进化成了我们现在分别在美味的三明治或煎蛋卷中提供的形式。“HC-05 串行 flash-hack 和无线蓝牙游戏手柄哪个先出现？“我们的猜测是[mitxela]想玩玩极其便宜的蓝牙模块，而构建无线控制器是后来才想到的。但是，这是一个很好的事后想法！(视频下方休息。)

这一切都始于 HC-05 蓝牙模块，该模块旨在传输串行数据，但可以通过简单的闪存 ROM 替换转换成十倍成本的通用设备。解决这一问题的通常方法需要通过并行端口进行位碰撞，但黑客们已经找到了一种方法，使用普通的 USB/串行适配器在位碰撞模式下做同样的事情。[mitxela]帖子的第一部分描述了这段冒险经历。

他的蓝牙模块现在可以作为游戏手柄使用，[mitxela]只需要一个游戏手柄就可以玩了。在易贝找到一个异国情调的老式 SNES 控制器后，他关掉了旧的逻辑，在导线上添加了磁线，还额外增加了一个 ATtiny2313，他就完成了！这是一个漂亮的控制器，在蓝牙中有定制的固件和定制的 ROM。美女！

[mitxela]对 Hackaday 并不陌生:我们以前报道过他的微型 MIDI 方波合成器。你真应该去看看他博客上的所有项目。

 [https://www.youtube.com/embed/fWXJDNcbZAA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fWXJDNcbZAA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 通用输入手势键盘

> 原文：<https://hackaday.com/2017/11/29/gesture-keyboard-for-universal-input/>

键盘是目前最普遍接受的计算机输入设备。它们可能是有线的、无线的或虚拟的，但很有可能你现在就在离键盘几厘米的地方。[Federico Terzi] [用 Arduino 和加速度计建造了一个原型](https://github.com/federico-terzi/gesture-keyboard)，这在概念上类似于 Palm 的旧涂鸦，尽管这个版本是在半空中用手持设备进行的，而不是在 LCD 屏幕底部的一个小正方形。他还可以通过蓝牙模块和电池进行无线操作。

Arduino 的任务是每当按下 12 毫米开关时，从加速度计获取数据，并将其输入计算机。每个字母都是由他的 Python 代码和 scikit-learn 的支持向量机单独学习的。没有什么能阻止用户给你喜欢的程序发单个字母的命令。例如，当你想投赞成票时，可以在 meatspace 竖起大拇指，或者捂住耳朵可以静音。

我们喜欢键盘黑客，比如这个[机械宏键盘](https://hackaday.com/2017/11/10/an-awesome-open-mechanical-keyboard/)，一个[最小且优雅的 USB 莫尔斯键(板)](https://hackaday.com/2017/10/03/a-vintage-morse-key-turned-into-usb-keyboard/)，还有布莱恩·本霍夫的[对机械键盘的公开情书](https://hackaday.com/2017/11/22/a-passion-for-the-best-is-in-mechanical-keyboards/)。

 [https://www.youtube.com/embed/OjTNS2ZKqRc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OjTNS2ZKqRc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示。
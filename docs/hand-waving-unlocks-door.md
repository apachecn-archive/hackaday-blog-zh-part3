# 挥手打开门

> 原文：<https://hackaday.com/2016/09/05/hand-waving-unlocks-door/>

谁不喜欢电影《少数派报告》中的用户界面呢?[汤姆·克鲁斯]只要在一个巨大的电脑屏幕前挥挥手就能操控它。[AdhamN]想用手势打开他的门。虽然它不像[汤姆]的好莱坞界面那样无缝，但它[设法完成了工作](http://www.instructables.com/id/Unlock-Your-Door-With-a-Hand-Gesture/)。你只需要在做手势的时候拿着你的智能手机。

该项目使用 Arduino 和伺服电机来来回移动螺栓。手势部分需要一个 1 遮板。这是一个与手机接口的板，允许您从 Arduino 程序中使用它的功能(在这种情况下是加速度计)。

剩下的应该很明显了。1sheeld 读取加速度计数据，当它看到正确的手势时，它会操作伺服系统。用智能手表来做这件事会很有趣，可能看起来不那么明显。

我们不久前讨论过[1 sheed](https://hackaday.com/2013/10/29/1sheeld-uses-your-smartphone-as-an-arduino-accessory/)板。当然，你也可以使用 [NFC](https://hackaday.com/2016/02/09/this-car-lets-you-fistbump-to-unlock/) 或其他一些传感器技术来触发机制。您可以在下面找到描述 1sheeld 的视频。

 [https://www.youtube.com/embed/3d3jJhdxGRI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3d3jJhdxGRI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


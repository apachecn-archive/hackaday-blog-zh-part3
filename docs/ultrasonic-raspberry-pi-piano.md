# 超声波树莓皮钢琴

> 原文：<https://hackaday.com/2017/04/22/ultrasonic-raspberry-pi-piano/>

便宜的东西让我们的创造力源源不断。恰当的例子？[安迪·格罗夫]建造了一个八传感器 HC-SR04 分线板，因为有问题的超声波距离传感器非常便宜，黑客很难避免按打订购它们。他最初是为机器人制造的，但后来只需要几行代码就可以把它变成一个手势可控的乐器。查看下面嵌入的视频，了解这些功能的概述。

他的 [Octasonic 分线板](https://www.tindie.com/products/andygrove73/octasonic-8-x-hc-sr04-ultrasonic-breakout-board/)只是一个伪装的 AVR 它从八个超声波传感器读取数据，并将单个 SPI 结果传递给任何其他充当大脑的控制器。在“piano”演示中，这是一个树莓 Pi，因此他需要通常的 5 V 至 3.3 V 电平转换。

剩下的是 Pi 上的代码，它使手势能够演奏音符，改变乐器，甚至关闭 Pi。Pi 代码是用 Rust 写的，[在 GitHub](https://github.com/TheGizmoDojo/UltrasonicPiPiano) 上面。一份[说明书有关于连接的更多细节。](https://www.instructables.com/id/Ultrasonic-Pi-Piano-With-Gesture-Controls/)

总而言之，用机器人零件建造一架“钢琴”肯定是一个有锤子的例子，每个问题看起来都像钉子，但我们发现一些由此产生的钉子雕塑就是这样产生的。这也不是我们第一次看到[八传感器超声波装置](http://hackaday.com/2017/02/25/octosonar-is-8x-better-than-monosonar/)。2017 年将会是超声波传感器项目年吗？

 [https://www.youtube.com/embed/Nc-wKYCPbVA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Nc-wKYCPbVA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


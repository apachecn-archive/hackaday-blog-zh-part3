# 电器显示器有点不稳定

> 原文：<https://hackaday.com/2017/01/08/shaky-appliance-monitor/>

许多人开始制造电器监控器，不管是冰箱、车库门还是洗衣机。通常情况下，最好不要切入电器进行直接电气连接，尤其是在涉及市电或水的情况下。但是我们如何知道设备在做什么呢？

[Drew Dormann]想改进他的旧洗衣机，所以设计了一个系统，使用一个振动传感器来监控电器。这是一个简单的构建，将 801s 振动传感器与 Raspberry Pi Zero 配对。很自然地，[适配器板随时可用](https://www.amazon.com/s/ref=nb_sb_noss?url=search-alias%3Dcomputers&field-keywords=801s+vibration+sensor)使连接东西变得容易。然后，只需用一个简单的 Python 脚本将它们捆绑在一起，该脚本使用 Twitter & PushBullet 发送通知。

值得注意的是，这种方法不仅仅局限于洗衣机，还有一系列家用电器都可以通过这种方式进行监控。很可能你甚至可以用这种方式窥探公共微波炉，尽管你可能会因为干扰而与 WiFi 信号中断做斗争。建造它并让我们知道。

[Drew]的构建是一个很好的例子，说明你可以在几个小时内用现成的零件组装起来。对于那些认为这种应用的 Pi 零过量的人来说，可以考虑这种基于 ESP8266 的[振动洗衣监控器。你认为你能做得更好吗？向我们展示你在](http://hackaday.com/2016/11/10/launitor-saves-you-from-accidentally-smelly-clothes/) [Hackaday.io](https://hackaday.io) 上的成果！
# WiFi 电源监控器

> 原文：<https://hackaday.com/2015/10/04/wifi-power-monitor/>

构建自己的硬件来测量交流功率并不是一件简单的事情。有许多东西需要测量，包括电压、电流、功率和功率因数。 [Atmel 90E24](http://www.atmel.com/devices/90E24.aspx) 是专为此目的设计的单芯片解决方案。连接几个元件，所有功率数据都可以通过 SPI 提供给微控制器。

[hwstar]基于该 IC 构建了定制的电源监控板。他的 [AC-Emeter](https://github.com/hwstar/HW-AC-Emeter) 将会给你你想要的所有测量值，并且包括一个用于数据收集和 WiFi 连接的 ESP12 模块。除了 Atmel 90E24 设备，还需要一个高功率低电阻电阻器用于[分流检测电流测量](https://en.wikipedia.org/wiki/Shunt_(electrical)#Use_in_current_measuring)。外部模块用于将电源电压转换为 5V，以便为电路板供电。

当然，在市电电压下工作可能是一件危险的事情。幸运的是，[hwstar]提供了一些关于如何防止“设备被炸毁”的技巧以及开源硬件和固件。

[通过[嵌入式实验室](http://embedded-lab.com/blog/?p=10761)
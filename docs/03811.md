# 用 Rpi_status 跟踪天气

> 原文：<https://hackaday.com/2016/10/13/keep-tabs-on-the-weather-with-rpi_status/>

[无名失败者]对简略的信息感兴趣。Glancable 设备是像汽车仪表板、手表或智能手机锁屏上的小部件这样的东西。本案中的简略信息发布系统为 [rpi_status](https://hackaday.io/project/9561-rpistatus) ，[启蒙树莓 pi 大赛](https://hackaday.io/contest/15532-enlightened-raspberry-pi-contest)中【无面者的】参赛作品。

[无脸失败者]将八个 WS2812 RGB LEDs 与一个由通用 ssd1306 控制器管理的小有机发光二极管屏幕耦合在一起。因为他正在为这个项目滚动自己的板，[匿名]一些按钮和一个 BMP180 温度传感器。使用像这样受欢迎的部件意味着像用于 WS2812 的 Pimoroni unicorn hat 库这样的库很容易获得。

像这样简单的显示可以显示任何东西——从每夜软件构建的状态，到早晨通勤的交通状况。[无脸失败者]用它来做天气数据。他的数据来源是 [Weather Underground 的](https://www.wunderground.com) API。天气信息显示在有机发光二极管上。WS2812 显示温度。一盏蓝色的灯意味着寒冷。随着温度升高，环会充满。蓝色八度后，颜色变为橙色，接着是红色。

休息之后，请观看视频，观看电路板的简短演示。

 [https://www.youtube.com/embed/py17ZlEoVJs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/py17ZlEoVJs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



![enpi](img/7d6ec196fe187128af3d9fd57fefe510.png)

**铺平学习道路，赢取奖品:**

* * *

### 进入[启蒙树莓 Pi 大赛](https://hackaday.io/contest/15532-enlightened-raspberry-pi-contest)！

只要教我们如何用圆周率做一些了不起的事情。([查看更多条目](https://hackaday.io/submissions/enlightened-raspberry-pi/list))
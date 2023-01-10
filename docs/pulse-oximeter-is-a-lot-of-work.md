# 脉搏血氧仪工作量很大

> 原文：<https://hackaday.com/2017/03/11/pulse-oximeter-is-a-lot-of-work/>

这些天我们有点被宠坏了。你可以抓取许多传感器，连接到你最喜欢的微控制器，加载一些简单的库代码，你就可以开始工作了。当[Raivis]得到 MAX30100 脉搏血氧仪分线板时，他认为它会像这样。它没有。他发现从设备中获得有用的结果需要大量的处理。幸运的是[他用 Arduino 代码写下了这一切](https://morf.lv/implementing-pulse-oximeter-using-max30100)。

脉搏血氧仪测量你的脉搏和血氧饱和度。你可能在医生办公室或医院的手指或耳垂上戴过这种东西。传统上，它们由一个红色 LED 和一个 IR LED 组成。探测器测量每种光通过的量，这两个量的比率与你血液中的含氧量有关。我们无法想象在 1935 年[Karl Matthes]是如何想出使用红光和绿光的，以及[Takuo Aoyagi](他和[Michio Kishi])是如何想出红外和红光部分的。

MAX30100 设法交替使用两个 led，调节它们的亮度，过滤读数中的线路噪声，以及其他一些任务。它将数据存储在缓冲区中。关键在于:你如何解读这个缓冲区？

[Raivis]显示了从缓冲区获取输出、移除 DC 分量、使其通过几个软件过滤器并检测心率的代码。要读取氧气读数，你还要做更多的工作。你可以在 [GitHub](https://github.com/xcoder123/MAX30100) 上找到该设备的代码。

如果你想在没有专用 IC 的情况下建造自己的，拿一个[晒衣夹](https://hackaday.com/2013/04/18/pulse-oximeter-from-lm324-led-and-photodiode/)。或者试试这个[更精致的建造](https://hackaday.com/2010/05/02/diy-pulse-oximeter/)。
# 感知帽子点亮圆周率

> 原文：<https://hackaday.com/2015/09/13/sense-hat-lights-up-pi/>

我们对 Raspberry Pi 的主要抱怨之一是它没有太多的 I/O。有很多附加组件，当然是为了扩展 I/O 功能。真正的 Raspberry Pi 基金会最近创建了 Sense Hat，它为 Pi 增加了许多功能，尽管它们可能不是我们想要的。这些板子是为 [AstroPi 项目](http://astro-pi.org/)(允许英国学校在太空进行实验的项目)制造的。他们似乎还没有正式向公众出售，但根据他们的网站，他们将很快出售。更新:尽管 Raspberry Pi 网站上的一些页面说它们还没有发布，[它们显然已经发布了。](https://www.raspberrypi.org/blog/buy-the-sense-hat-as-seen-in-space/)

该板有一个 ATTiny，但它不应该是用户可编程的(尽管我们在这里嗅到了未来的黑客)。有一个 Python API，据推测，CPU 正在运行类似于 [Firmata](https://www.arduino.cc/en/Reference/Firmata) 的东西。不过，最明显的特点是 8X8 RGB LED 矩阵。这可以用于(非常低的分辨率)图形输出或滚动文本。还有一个五按钮操纵杆和一系列 I2C 传感器，包括惯性测量传感器以及压力、湿度和温度传感器。此外，还有几个 3D 传感器，包括加速度计、陀螺仪和磁力计。

需要更传统的 I/O 吗？如果[你需要或者更类似的](http://hackaday.com/2013/03/22/analog-input-expansion-boards-for-raspberry-pi/)，或者甚至仅仅是[奴役一个 Arduino](http://hackaday.com/2014/09/09/adding-io-to-the-rasberry-pi-models-a-b/) ，你可能想要自制你自己的扩展。

这顶帽子有着奇怪的设备组合，但是有很多有趣的可能性。我们希望我们可以坚持一个词，而不是帽子，盾牌，斗篷，以及其他供应商不断发明的东西。我们一直建议使用“水蛭”,但是没有一个营销人员会让这个建议通过他们。我们满足于女儿董事会。

由于只有少数人从第一轮开始就有这种帽子(更新:它们从八月下旬才开始公开销售)，所以还没有太多的项目。但看看下面的视频，包括我们看到它时首先想到的使用 8×8 矩阵的视频:康威的《生命的游戏》。

 [https://www.youtube.com/embed/kNM3AUeJYek?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kNM3AUeJYek?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


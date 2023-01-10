# 来自 RGB LED 和光电池的颜色传感器

> 原文：<https://hackaday.com/2017/08/29/color-sensor-from-an-rgb-led-and-a-photocell/>

当你需要量化一个物体的颜色时，你有很多选择。你可以用 Raspberry Pi 相机和 OpenCV 来解决这个问题，并通过软件来解决它，或者你可以购买现成的 RGB 传感器，并将其连接到 Arduino。或者你可以回归基础，用 LED 和光电池制作[这个反射式 RGB 传感器。](https://www.instructables.com/id/How-to-Use-RGB-LEDs-to-Identify-Colours-DIY-Colour/)

[TechMartian]方法背后的原理很简单:用不同颜色的光照射一个物体，然后测量它反射了多少光。如果你知道对应于最大反射率的光的红色、绿色和蓝色成分，那么你就知道物体的颜色。他们的传感器使用四引脚 RGB LED，但我们认为也可以使用新像素。光电传感器是一个简单的硫化镉电池，当 Arduino 用 PWM 信号驱动 LED 通过所有可能的颜色时，它可以测量从物体反射回来的光的强度。传感器在使用前需要白平衡，但在下面的视频中似乎给出了合理的结果。有人认为，无微控制器的设计也是可能的，555 扫描 PWN 信号，运算放大器负责检测。

好的 RGB 传感器的自然终点是什么？糖果分拣员，或者说是理所当然的，我们有很多这样的例子，从[光滑精致的](http://hackaday.com/2017/02/06/mms-and-skittles-sorting-machine-is-both-entertainment-and-utility/)到[稍微粗糙一点的](http://hackaday.com/2014/12/14/taste-the-rainbow-one-color-at-a-time/)。

 [https://www.youtube.com/embed/7zMZvkKZtFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7zMZvkKZtFI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


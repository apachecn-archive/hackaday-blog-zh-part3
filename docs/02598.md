# 宜家投射灯改造增加了 LED 矩阵和树莓 Pi Zero

> 原文：<https://hackaday.com/2016/06/14/projection-lamp-makeover-adds-led-matrix-and-raspberry-pi-zero/>

如果你和我们一样，很难不在脑海中将宜家的所有东西都分解成其他东西。沙拉碗？抛物面天线。抽屉滑轨？线性运动轨道。存储容器？蚀刻槽。我们承认，我们仍然没有想出如何处理那 1000 包茶灯。

[Alain Mauer]实现了我们梦寐以求的宜家黑客技术。特别是，他[拿着 Sprida 投射灯](https://hackaday.io/project/12084/instructions)把一个 8×8 的 LED 矩阵和 Raspberry Pi Zero 塞进去。

有问题的灯实际上是儿童用的幻灯机。在[Alain]拿到它之前，它的后面有一个 LED，中间有一个幻灯片支架，前面有一个聚焦镜头。他的方法很简单:去掉 LED 和透明胶片，把 LED 矩阵放在幻灯片原来所在的焦平面上。在软件中反转 LED 上的图像来补偿镜头，就大功告成了。

~~视频上写着“带 WiFi 的树莓派 Zero”，项目标题承诺“物联网”，但我们在 build 中没有看到 WiFi。我们猜测[Alain]会找到时间做这件事——[这很容易做到](http://hackaday.com/2016/04/21/usb-less-wifi-for-the-pi-zero/)~~ 。(Doh！有一个小小的 USB WiFi 加密狗提供强制性的无线连接。)无论如何，重点是投影，我们喜欢它，如果我们说它不会让我们想到 RGB 矩阵，那我们就是在撒谎。

 [https://www.youtube.com/embed/6D7-UXovsY4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6D7-UXovsY4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


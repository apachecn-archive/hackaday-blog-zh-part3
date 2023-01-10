# 袖珍投影仪使用树莓派

> 原文：<https://hackaday.com/2018/06/06/pocket-projector-uses-raspberry-pi/>

谁不想要一个袖珍~~保护器~~ [投影仪](https://www.electromaker.io/blog/article/make-your-own-portable-pocket-sized-pi-zero-powered-projector)？没有什么比拿出一份你最近去漫画书大会的幻灯片更能打动约会对象了。[MickMake]构建的关键是德州仪器价值 100 美元的 DLP2000EVM 评估模块。这是一个便宜的光引擎，非常适合滚动你自己的投影仪。你可以在下面的视频中看到结果。

如果你不需要紧凑，你可以用任何 Rasberry Pi 甚至普通计算机来驱动这个模块。但是要得到那个袖珍外形，一个 Pi Zero W 符合要求。来自[MickMake]的定制 PCB 使该板能够以非常小的尺寸与 DLP 模块相匹配。

DLP 芯片使用许多显微镜，你可以在电脑控制下移动大约 20 度。所以你可以把光线反射到镜头里或者反射出去，这样图像就变成黑色了。对于颜色，RGB LED 在原色中循环，你必须根据你想要投射的颜色来调整镜子的移动时间。当然，模块会在幕后为您处理所有这些事情。

该模块可以输出高达 30 流明(默认情况下，这是 20 流明)，并具有 I2C 和 8/16/24 位并行 RGB 视频接口。如果你不想使用定制板，该设备支持开箱即用的 BeagleBone Black。DLP 分辨率为 nHD。即反射镜阵列为 640×360。虽然你可能认为“n”代表零，但它实际上代表九分之一。

当前版本的适配器板缺少音频放大器，尽管在将来的版本中可能会有所改变。现在，你可以通过蓝牙从 Pi 播放音频。

我们很惊讶我们还没有在 3D 打印机中看到这种廉价的模块。或者也许是一个[假日放映机](https://hackaday.com/2018/01/22/teardown-christmas-laser-projector/)项目。忙起来，完成后通过[举报热线](https://hackaday.com/submit-a-tip/)通知我们。

 [https://www.youtube.com/embed/XFciR-U7yhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XFciR-U7yhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


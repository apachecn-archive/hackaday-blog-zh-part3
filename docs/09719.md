# FPGA 坚持不懈里克滚动你

> 原文：<https://hackaday.com/2018/06/11/fpga-persistently-rick-rolls-you/>

当[Im-pro]想要一个显示器时，他希望它旋转。因此，他建造了一个能够以每秒 16 帧的速度显示 131 x 131 像素的 12 位彩色图像的视觉暂留显示器。你可以在下面看到一个关于这个项目的视频，但是不要担心，你可以在你的普通显示器上观看。

该项目从 PC 上基于 Java 的屏幕截图开始。数据通过无线传输到 ESP8266 的显示屏。然而，实际的显示驱动是由 FPGA 完成的，它驱动电机，读取霍尔效应指数传感器，并点亮 led。

也许该项目的最有趣的部分是基于 FPGA 的输入视频的直角坐标到显示器所需的极坐标的映射。有 4 个 led 臂或“翅膀”和一个 3D 打印结构，都包含在帖子中。

FPGA 是一个 Cmod S6，它是 Xilinx Spartan 6 的分线板，处理工作负载绰绰有余。还涉及定制 PCB，所以当你考虑它时，它是一个相当广泛的项目。Java 软件、ESP8266 软件、FPGA 配置、3D 打印设计和 PCB 布局。如果你想做一些简单的事情，但又有一点面面俱到，这可能是你的下一个项目。

我们看到的大多数 POV 显示器都没有这种颜色深度和分辨率。我们已经看到了围绕着风扇建造的显示屏[。然而，我们最喜欢的是](https://hackaday.com/2018/04/21/building-a-pov-display-on-a-pc-fan/)[狗速度计](https://hackaday.com/2017/10/07/dog-pov-canine-speed-indicator/)。

 [https://www.youtube.com/embed/yG3uugdAIMQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yG3uugdAIMQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


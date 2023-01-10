# 需要一千个额外的 PWM 引脚吗？

> 原文：<https://hackaday.com/2018/04/11/need-a-thousand-extra-pwm-pins/>

如果您的 Arduino 用完了 I/O 线路，您可以随时添加几个 I/O 扩展器芯片中的一个，它采用串行接口来设置它的几个引脚。或者你可以买一个 Arduino Mega，它有额外的插座来满足你的需求。但是如果你真的需要更多的别针，比如说一千个，你会怎么做呢？或许[布莱恩·洛]有答案。好吧，完全公开:如果你真的需要一千个，这个视频并不完全适合你，因为他向你展示了如何添加多达 992 个 PWM 输出。他使用的芯片可以与任何微控制器一起工作(视频显示的是 ESP8266)，我们认为你可以使用其中的两个菊花链，轻松突破 1000 大关。

我们喜欢视频有多短(短短两分钟；见下文)因为它得到了正确的点。PCA9685 芯片通过 I2C 接口提供 16 个 12 位 PWM 通道。您可以菊花链连接多达 62 块电路板，以获得承诺的 992 路输出。

[Brian]使用廉价的 2 美元分线板，让您设置 6 位地址，有一个漂亮的电源连接器，使它易于使用小型表面贴装设备。板上的 16 路输出可以有独立的占空比，但它们共用一个输出频率。这意味着，如果你想将一些通道用于电机等低频设备，将一些通道用于 led 等高频设备，你可能需要为两块电路板支付 4 美元。

在 Hackaday.io 上，我们已经看到这些设备[驱动 128 个振动马达](https://hackaday.com/2017/09/22/hackaday-prize-entry-haptivision-creates-a-net-of-vibration-motors/)。PCA9685 让我们想起了使用 FPGA 将我们自己的[串行转换为 PWM 器件的时代。](https://hackaday.com/2015/12/17/pwm-on-the-lattice-icestick/)

 [https://www.youtube.com/embed/MB9DGwyGguw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MB9DGwyGguw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


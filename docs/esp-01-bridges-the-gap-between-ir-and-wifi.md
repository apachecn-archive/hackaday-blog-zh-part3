# ESP-01 填补了红外和无线网络之间的空白

> 原文：<https://hackaday.com/2018/02/20/esp-01-bridges-the-gap-between-ir-and-wifi/>

[埃米利奥·菲卡拉]最近给我们写了一封短信，讲述了他努力把他的电视机和接收器拖进现代社会。他的电视太旧了，需要一个外部调谐器，这意味着它需要两个独立的遥控器来正确地浏览频道。他想简化这种情况，并认为在这样做的同时，他还可以通过 WiFi 控制整个事情。

为了开始这个项目，[Emilio]必须捕捉他想要模仿的两个遥控器的红外信号。他用垃圾箱里的零件组装了一个快速的小红外接收器，可以连接到他电脑的麦克风端口。然后，他使用一个[开源红外协议分析器](http://www.ostan.cz/IR_protocol_analyzer/)来捕获代码，并将它们解码成十六进制值。

作为概念验证，他想出了一个结合了 ESP-01 和 ATmega88 的小装置。ESP-01 运行一个最小的 web 服务器，它接收十六进制代码作为 URL 查询字符串。这些十六进制代码随后由 ATmega88 解释并通过红外 LED 发送出去。[Emilio]指出，直接从 ATmega 引脚驱动 IR LED 会产生相当低的范围，约为 1 米，但这对于他的目的来说已经足够了。如果你想用更大的功率驱动红外 LED，你需要增加一个晶体管来完成开关。

[![](img/4976ccd53f3b28b6222a531ef215ab94.png)](https://hackaday.com/wp-content/uploads/2018/02/irwifi_detail2.png)

Passing the hex code 0x0408 to turn off the TV

现在，他可以解码来自原始遥控器的信号，并通过他的桥接设备在 WiFi 上传输它们，他已经具备了推出一款流线型家庭娱乐控制器所需的所有基础。为他的智能手机开发一个本地应用程序，或者一个最小的网络界面，这是拼图的最后一块。

这个项目让我们想起了类似的尝试[通过蓝牙](https://hackaday.com/2015/06/19/ir-remote-for-smartphone-via-bluetooth-adapter/)从智能手机控制传统的红外设备。如果你正在寻找更多关于从你的微控制器获取红外信号的信息，[这本 2013 年的入门书仍然是这个主题的绝佳视角。](https://hackaday.com/2013/11/20/primer-tutorials-for-arduino-ir-remote-cloning-and-keyboard-simulation/)
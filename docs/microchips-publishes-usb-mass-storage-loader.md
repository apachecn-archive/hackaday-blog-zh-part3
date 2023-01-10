# 微芯片发布 USB 大容量存储加载器

> 原文：<https://hackaday.com/2016/03/11/microchips-publishes-usb-mass-storage-loader/>

微芯片刚刚[发布了他们的 USB-MSD 编程器固件](https://github.com/MicrochipTech/XPRESS-Loader)。这个开源项目允许一个板枚举为一个 USB 大容量存储设备。编程就像将一个. hex 文件复制到“驱动器”一样简单。

这些代码是在[上个月发布的 10 美元 Xpress 板上运行的](http://hackaday.com/2016/02/15/microchip-unveils-online-mplab-ide-and-10-board/)，它包括一个 PIC18F25K50，作为实际目标微处理器的 PICkit On Board (PKOB)编程器；一张 PIC16F18855。在其股票版本中，XPRESS-Loader 固件对任何行大小为 32 个字的 PIC16F188xx 芯片进行编程。但是，应该可以调整这个软件包，对任何使用 8 位 LVP-ICSP 协议的芯片进行编程。

乍一看，这似乎是个小问题:它需要在主板上安装两个微控制器，并且只能对大量 PIC 库存中的一小部分进行编程。但在我们看来，USB MSD 才是杀手，因为它不需要任何软件或驱动程序。这对各种黑客来说都是一个巨大的邀请。但是，不久之后，Xpress 团队还会推出更多产品。

原来[Voja Antonic]选择在[hack aday | Belgrade 徽章](https://hackaday.com/2016/02/17/its-alive-badge-for-hackaday-belgrade/)上使用的微控制器是 25k50。自从听说 Xpress 板后，我们一直在与一些 PIC 工程师交谈，他们正在开发一种可以在同一芯片上编程的加载器。这意味着无需特殊硬件或驱动程序的设备升级——非常适合会议上的徽章黑客攻击。这可以通过一个预编译的十六进制来完成，它是在 MPLAB X、 [MPLAB Xpress](http://mplabxpress.microchip.com/) 或其他平台上创建的。如果我们听到更多关于这个项目的消息，我们会及时通知你。
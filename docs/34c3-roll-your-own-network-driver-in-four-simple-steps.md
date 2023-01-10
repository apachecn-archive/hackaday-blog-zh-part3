# 34C3:用四个简单的步骤推出你自己的网络驱动程序

> 原文：<https://hackaday.com/2018/01/01/34c3-roll-your-own-network-driver-in-four-simple-steps/>

编写自己的驱动程序是一门特殊的学科。驱动程序一方面与外部硬件紧密配合，同时又深深地扎根于操作系统中。那是一个问题中的两种专门化。近年来，许多专用网络硬件正被软件所取代。[保罗·埃梅里希]是致力于提高这些系统性能的研究人员。

让软件像网络硬件一样工作需要能够快速处理大量小数据包的驱动程序，这是标准 API 没有设计的。在今年的混沌通信大会上，Paul 剖析了编写这种特殊风格的驱动程序的不同方法，并解释了每种方法的缺点。

[https://media.ccc.de/v/34c3-9159-demystifying_network_cards/oembed](https://media.ccc.de/v/34c3-9159-demystifying_network_cards/oembed)

[Paul]向我们介绍了英特尔 ixgbe 系列网卡，这些网卡非常适合此类工作，因为它们很常见，有很好的文档记录，并且具有易于使用的固件。演讲的后半部分深入到为这些卡编写一个[用户空间驱动](https://github.com/Emmericp/ixy)的细节。重点是如何正确地为 DMA 分配内存，以及如果在这里出错，文件系统会发生什么。

另一个体验编写驱动程序的好项目是这个旧的翻转点显示的项目。对于那些喜欢摆弄自己的以太网硬件的人来说，[将它添加到一个 ESP32](https://hackaday.com/2017/04/18/enabling-ethernet-on-the-esp32/) 是一个不错的选择。
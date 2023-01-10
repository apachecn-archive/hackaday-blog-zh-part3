# Hackaday 奖参赛作品:USB 数据包窥探

> 原文：<https://hackaday.com/2017/07/25/hackaday-prize-entry-usb-packet-snooping/>

有时候你在开发自己的硬件时会遇到一些问题，为了解决这些问题，你必须开发自己的工具。这就是[KC Lee]的 [USB 数据包监听器是如何创建的](https://hackaday.io/project/20532-usb-packet-snooping)。这是一个小设备，允许捕捉和分析全速 USB 流量，以调试[KC]的*其他*黑客奖条目之一。

[KC]正在为今年的 Hackaday 奖制作一个 HID 多媒体拨号盘。这有点像微软的 Surface Dial 或无处不在的 Griffin PowerMate，它们已经在市场上销售了 20 多年。这个多媒体拨号盘使用 STM8 对 USB 进行位碰撞，这意味着[KC]需要一个工具来捕获原始 USB 数据包。

这个 USB 数据包嗅探器的设计分为两部分。第一种是加密狗或直通设备，仅用作 USB 设备和 USB 主机之间的分接头。记录和分析板连接到这个加密狗，并使用一个相当快速的 ARM 微控制器来监听 USB 数据包，并通过串行将所有内容发送到 PC。

这是一个相当新颖的装置； [V-USB](https://www.obdev.at/products/vusb/index.html) 仅限于低速 USB，其他 USB 捕获工具远远超出了爱好者的预算。PC 上的软件解决方案显然行不通，因为[KC]甚至不知道他是否在发送有效的 USB 数据包。这是一个伟大的工具，最终将业余爱好者级别的 USB 分析提升到全速 USB。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
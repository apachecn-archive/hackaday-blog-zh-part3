# 用于远程显示器 LoRaWAN 和 Raspberry Pi 计算模块

> 原文：<https://hackaday.com/2017/02/08/lorawan-and-raspberry-pi-compute-module-for-a-remote-display/>

我们在这些页面上看到了许多 Raspberry Pi 项目，这些项目包含了剑桥小黑板的所有变体，但有一个明显的例外。令人惊讶的是，他们中很少有人采用它的工业嵌入式表亲 Raspberry Pi 计算模块。Pi-on-a-SODIMM 外形是一个不错的想法，但我们猜测，相对于 B 型或 Pi Zero，开发板的价格较高，这促使我们社区的大多数人选择后者。

[Andrew Back]在 RS DesignSpark 网站上发布了一个简单的演示项目，介绍了计算模块 3，[使用它来运行远程操作的显示器](https://www.rs-online.com/designspark/making-a-remotely-updated-display-with-the-raspberry-pi-compute-module-3-and-microchip-rn2483)。此外，它使用 RN2483 LoRaWan 无线电模块和[物联网](https://www.thethingsnetwork.org/)进行通信，这使得它值得一看，即使计算模块不感兴趣。

我们完成了启动模块和安装操作系统的过程，以及设置 LoRaWAN 和物联网连接的过程。然后，我们将学习 Python 代码，它将所有这些整合在一起，并使用 PyGame 写入显示。

你可能会指出，它可以轻松地使用其他 Pi 板来完成这项工作，你是对的，但重要的是要记住，这是一个演示项目，旨在让你开始使用该平台，因此这是一个有趣的阅读，即使我们许多人从未使用过计算模块。

我们报道了 2014 年[计算模块发布](http://hackaday.com/2014/04/07/the-raspberry-pi-compute-module/)和上个月[最新版本](http://hackaday.com/2017/01/16/raspberry-pi-launches-compute-module-3/)的发布。也许我们会开始看到我们这个级别的一些项目使用它，而不是传统的 Pi 板，现在它有了更快的版本。
# 对 BLE 服务进行逆向工程以控制灯泡

> 原文：<https://hackaday.com/2017/08/13/reverse-engineering-a-ble-service-to-control-a-light-bulb/>

所以，你买了一个物联网灯泡，这是一个有趣的玩具，只需轻触一个应用程序，就可以让你的环境沐浴在美丽的色彩中，但最终你会想要更多。你开始考虑如何利用它做更多的事情，并开始研究它的内部运作。然后，令你惊恐的是，你发现你买的设备远没有一个方便的 API 供你使用，它有一个难以理解的封闭协议，无法轻易访问。

这是[Ayan Pahwa]在购买 Syska Smartlight 彩虹 LED 灯泡时面临的问题，他发现其蓝牙低能耗接口使用了封闭协议。但他没有放弃，而是继续对灯泡和应用程序之间的通信进行逆向工程，他的文章是一篇有趣的读物，为门外汉提供了一些 BLE 工作的基本入门。

BLE 允许设备制造商定义他们自己的设备服务，这些服务专用于他们的功能以及通用设备类型的标准服务。使用 Nordic Semiconductor 提供的一个方便的 Android 应用程序，他能够识别为灯泡定义的服务，但遗憾的是，它们缺乏任何人类可读的信息来帮助他了解它们的目的。因此，他不得不直接嗅探 BLE 数据包，由于缺乏专用硬件，他依赖于自 KitKat 以来内置于 Android 版本的开发人员功能，允许捕获和记录数据包。通过分析产生的包文件，他能够识别灯泡内的德州仪器芯片，并推断出控制其颜色所需的序列。然后他可以使用 Bluez 工具直接与它对话，就像变魔术一样，他的颜色出现了！看看我们放在休息下面的视频。

我们中的许多人可能永远不需要对 BLE 设备进行逆向工程。但是，如果我们是 BLE 的新手，在读完[Ayan]的文章后，我们至少会对它的内部运作有所了解。这只能是一件积极的事情。

 [https://www.youtube.com/embed/g1_8cY--fIM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g1_8cY--fIM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



想更多地了解 BLE 吗？在上面阅读我们的日常词典。如果你想使用它，看看这个[微型 BLE UART](http://hackaday.com/2016/04/06/tiny-ble-uart-makes-bluetooth-low-energy-simple/) ，或者甚至[使用 NRF24L01 模块](http://hackaday.com/2013/09/21/sending-data-over-bluetooth-low-energy-with-a-cheap-nrf24l01-module/)。
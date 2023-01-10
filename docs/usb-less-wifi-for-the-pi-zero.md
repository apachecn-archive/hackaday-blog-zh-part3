# 用于 Pi Zero 的无 less WiFi

> 原文：<https://hackaday.com/2016/04/21/usb-less-wifi-for-the-pi-zero/>

自从 Raspberry Pi Zero 推出以来，黑客、制造商和爱好者的电子世界陷入了混乱。批评者说，树莓圆周率基金会是腐败的，圆周率零点只是一个让他们出名的营销策略。其他人附和说，树莓派零甚至不存在。不管一百万只猴子在一百万个键盘上说什么，树莓派 Zero 确实存在，而且非常酷，尽管它是多么有限。只有一个 USB 口，但不代表不能有 WiFi。[ajlitt]为 Pi Zero [设计了一个 WiFi 帽，它可以直接通过 GPIO 引脚](https://hackaday.io/project/8678-rpi-wifi)，并且在任何树莓 Pi 上实现不会花费超过几美元。

Pi 上没有以太网端口，除了一个 USB OTG 端口之外，没有明显的通往外界的高速接口。另一方面，Pi 上的 SoC 中隐藏了一些东西，包括两个 MMC 控制器。其中一个控制器用于 SD 卡，但第二个控制器可以在几个 GPIO 引脚上断开。通过接入这些引脚并正确配置内核，SDIO 在 GPIO 引脚上可用，通过廉价的 ESP8266 模块提供 Pi WiFi。

在之前，我们已经看过【ajlitt】在圆周率上的 [SDIO 设备的工作，但是他已经慢慢地在考虑圆周率零点的情况下重新制作了这个版本。它不是作为 Hackaday 奖的一个项目开始的，但它已经是迄今为止最受欢迎的作品之一。当然，Hackaday.io 上有数千个项目*没有进入今年的 Hackaday 奖，如果你落后于其中的一个，这是你站出来的呼吁。*](http://hackaday.com/2015/12/09/raspberry-pi-wifi-through-sdio/)

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)
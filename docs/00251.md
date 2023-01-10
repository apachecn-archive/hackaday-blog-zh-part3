# Arduino 期待已久的改进 WiFi 盾

> 原文：<https://hackaday.com/2015/10/01/arduinos-long-awaited-improved-wifi-shield/>

在 2014 年纽约创客大会上宣布，[最新的 Arduino WiFi shield 终于上市了](https://blog.arduino.cc/2015/09/30/arduino-wifi-shield-101-available-in-the-store/)。这个盾牌取代了旧的 Arduino WiFi 盾牌，同时提供了一些简洁的功能，这些功能将非常方便地用于尚未开发的物联网。

虽然 WiFi Shield 101 是在一年前发布的，但它的功能非常有趣。新的 WiFi shield 支持 802.11n，由于 Atmel 的一些加密芯片产品，这个 shield 是第一个支持 SSL 的官方 Arduino 产品。

新的 Arduino WiFi Shield 101 具有一个用于 802.11 b/g/n WiFi 连接的 [Atmel ATWINC1500](http://www.atmel.com/devices/atwinc1500.aspx) 模块。这个模块，像十几个其他 WiFi 模块一样，处理 WiFi 协议的繁重工作，包括 TCP 和 UDP 协议，让 Arduino 的其余部分自由地做实际工作。虽然随着这些网络变得越来越普遍，802.11n 的加入将会越来越受欢迎，但是~n 提供的速度实际上并不适用；你不会以 300 Mbps 的速度从 Arduino 中推出比特。

WiFi 盾上还包括一个 [ATECC508A](http://www.atmel.com/devices/ATECC508A.aspx) 加密认证芯片。这可能是对旧的 Arduino WiFi shield 最有趣的改进，并为即将到来的物联网提供了更大的安全性。已经在太空中的 WiFi 模块都有自己对 SSL 的支持，包括 [TI 的 CC3200](http://processors.wiki.ti.com/index.php/CC32xx_SSL_Demo_Application) 系列模块、 [Particle](https://www.particle.io/) 的物联网模块，以及对 ESP8266 的一些支持。
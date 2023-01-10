# 使用 ESP8266 注入数据包

> 原文：<https://hackaday.com/2016/01/14/inject-packets-with-an-esp8266/>

[Kripthor]给我们发了一个他博客的链接，在那里他写了低层网络的 Hello World。基本上，他在构建自己的数据包并发送出去。这本身并不是一件坏事。你可以将这种力量用于各种网络——诊断用途。因此，尽管他的博客帖子有个不祥的名字“ESP8266 干扰”，但他并没有真的做什么坏事——他只是创建了许多假的 WiFi [信标帧](https://en.wikipedia.org/wiki/Beacon_frame)，并不时地将它们发送出去。

这显然会对一些易受攻击的路由器造成不良影响。谁知道呢？想测试你的吗？

自然，我们想看看他是如何做到的，我们在 GitHub 中公开了[Arduino 代码。原来，Espressif 已经编写了一个`wifi_send_pkt_freedom()`函数，它只是将您想要的任何数据包发送到网络。那很容易。](https://github.com/kripthor/WiFiBeaconJam/blob/master/WiFiBeaconJam.ino)

此外，ESP8266 将进入监控模式，在这种模式下，它会监听所有 WiFi 流量，而不管它指向的 MAC 地址。[Pulkin]似乎已经为我们完成了这项工作，[在他的 GitHub](https://github.com/pulkin/esp8266-injection-example) 中发布了代码。现在事情变得很糟糕。将混杂监控模式与一些精心构建的管理框架结合起来，最终可能会在一个 2 美元的硬件上产生一个[经典的 WiFi 拒绝服务攻击](http://hackaday.com/2011/10/04/wifi-jamming-via-deauthentication-packets/)。

我们认为 ESP8266 具有如此强大的功能非常酷，我们恳请大家负责任地使用它。我们最不希望看到的是这个世界充满了 WiFi-DOS 垃圾。你最不想看到的就是联邦通信委员会的来访。
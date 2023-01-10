# Belkin WeMo 拆卸

> 原文：<https://hackaday.com/2015/11/17/belkin-wemo-teardown/>

EDN 的[Brian Dipert]对 Belkin 对物联网(IoT)热潮的回应进行了驳斥:WeMo。这个小小的 WiFi 小工具插在插座上，让你通过智能手机应用程序或类似亚马逊 Echo 的东西打开和关闭连接的设备。

正如你可能会从一个廉价的消费类硬件中期待的那样，里面并没有太多东西。数字板包含一个 Ralink WiFi 芯片，一个蚀刻在 PCB 上的天线，以及一些组件，包括 SDRAM 和一些闪存。

Ralink 芯片通常用于无线接入点/路由器，WeMo 使用该功能进行配置。如果你曾经配置过谷歌 Chromecast，过程是类似的。WeMo 创建自己的 WiFi 网络供您连接。然后，您可以将其配置为连接到您的首选网络。

第二块板有交流接口，它使用一个很好的老式继电器将交流插座的火线切换到负载。零线和地线只是简单地穿过。

我们已经破解了 WeMo 几次，包括如何制作假的 WeMo 设备以及如何使用 UART 将[破解成一个 WeMo 设备。我们甚至找到了](http://hackaday.com/2014/08/09/defcon-22-hack-all-the-things/#more-128722)[一个把 OpenWRT 放到东西上的教程。](http://sheldor.blogspot.de/2014/01/openwrt-for-wemo-part-1-compiling.html)我们很惊讶我们没有看到更多 WeMo 黑客——你对我们有所隐瞒吗？请在评论中告诉我们。

如果你以前没有遇到过 WeMo，你可以在下面的视频中看到它是如何为用户工作的。

 [https://www.youtube.com/embed/kcexu1xGyN0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kcexu1xGyN0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


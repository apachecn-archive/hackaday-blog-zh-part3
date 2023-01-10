# 你长椅上的无线中继器

> 原文：<https://hackaday.com/2017/12/25/the-wifi-repeater-you-probably-have-on-your-bench/>

没有什么比时好时坏的 WiFi 信号更令人沮丧的了。在公共网络上已经够糟了，但在家里呢？即使你可以忍受，如果你的同居者没有可靠的无线网络，他们肯定会影响你的技术能力。一种解决方案是 WiFi 中继器。当然可以买一个。但是你也可以用一个 [ESP8266 和一些来自 GitHub](https://github.com/martin-ger/esp_wifi_repeater) 的代码做一个。下面还有一个关于该项目的视频。

[Martin Ger 的]代码实现了 NAT，所以它不是一个真正的 WiFi 中继器，而更像是一个网桥或路由器。当然，这意味着性能不是一流的，但测试显示它可以保持大约 5 Mbps，这对于一个价值几美元的小主板来说并不坏。有 8 个客户端的限制，但是对于很多情况来说已经足够了。即使你不想把它用作路由器，它也有一个网状模式，可以作为一些有趣项目的基础。

有一个基于 web 的通用设置配置，以及一个位于端口 7777 或串行端口上的控制台，用于执行端口映射或静态 DHCP 寻址等高级操作。有一个简单的防火墙和一个内置的 [MQTT 客户端](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)。

另一个巧妙的特性是可选的 automesh 模式，它允许几个中继器进行自组织。为此，[Martin]需要一种方法来了解哪些中继器接近“真正的”WiFi。在这种模式下，中继器实际上会改变其 MAC 地址来提供此信息。至少可以说，这是一个不寻常的解决方案。MAC 地址都以 24:24 开始，以避开其他设备，但设备动态更改其 MAC 地址是很奇怪的。也可能是创造性的，我们无法决定。

如果只是想扩展自己自制的 RS232 网络，[还是可以用一个 ESP8266](https://hackaday.com/2015/09/18/transparent-esp8266-wifi-to-serial-bridge/) 。当然，这不是我们看到的第一款替代商业消费品[的 ESP8266。](https://hackaday.com/2017/09/30/lameboy-is-handheld-gaming-on-the-esp8266/)

 [https://www.youtube.com/embed/OM2FqnMFCLw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OM2FqnMFCLw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


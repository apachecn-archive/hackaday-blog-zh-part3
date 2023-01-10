# ESP32 测试版到达

> 原文：<https://hackaday.com/2015/12/23/the-esp32-beta-units-arrive/>

一年多前，ESP8266 WiFi 模块[平静地出现在 Seeed Studio 的商店](http://hackaday.com/2014/08/26/new-chip-alert-the-esp8266-wifi-module-its-5/)。从那以后，文档被翻译成了英语，为这个芯片创建了一个合适的开发环境，每个人都在使用这个便宜但功能强大的芯片用于最新的物联网。

ESP8266 背后的公司 Espressif 并没有固步自封，几个月来，他们一直在研究下一代强大的 WiFi 微型廉价系统。他们有了硅芯片，已经有 200 名幸运儿拿到了 ESP32 的第一批测试设备，这是 Espressif 的下一代 WiFi 芯片。拆卸工作已经开始，【lady ada】[将她对芯片的初步实验传输到中间管道](https://www.youtube.com/watch?v=HCGHb0OVz1s)(见下文)。【马丁】也是收到这些早期测试芯片 [的家伙之一，他很好心地在 Espressif 的最新芯片](https://harizanov.com/2015/12/esp32/) 上发表了自己的想法。

关于[ESP32 的一点信息已经流出](http://hackaday.com/2015/12/08/more-esp32-info-dribbles-out/)，【LadyAda】和【Martin】的演示单元证实了我们所有的怀疑。有两个运行频率高达 160MHz 的 Tensilica L108 处理器，许多外设，包括 ADC、DAC、I2C、SPI、I2S 和 PWM，更多 RAM、AES 和 SSL 用于安全，以及蓝牙低功耗。WiFi 也进行了升级，ESP32 将支持高达 150 Mbps 的速度。

分发给开发人员的测试单元实际上是 Espressif 的内部开发单元，标签为 ESP31B，当前主板的外形尚未确定将会推出什么。这些 beta 单元是具有 1.27 毫米间距的齿形垫的板；这并不完全是一个用户友好的软件包，而且人们[已经破坏了测试版](http://esp32.com/viewtopic.php?f=2&t=41&sid=b0ac665492ab81217c434d4fead64f85)。

虽然功能很棒，但 Espressif 说[ESP32 不是 ESP8266](https://twitter.com/espressifsystem/status/663056719279292416) 的替代品。它们是不同的市场，如果您只是想在项目中添加 WiFi，没有理由不选择 ESP8266。

这种新芯片带来了许多新的可能性。Espressif 的工作人员正在对他们的内部测试版(ESP31)进行大量实验。[Sprite_tm]也在为 Espressif 工作，所以你知道会有一些非常酷的演示项目，比如[一个世嘉主系统仿真器](http://esp32.com/viewtopic.php?f=2&t=53)，[带视频](https://www.youtube.com/watch?v=OVZnVhBfNuo)。这只是 SMSPlus 仿真器到 ESP31 的一个端口，LCD 通过 SPI 以 15fps 的速度驱动。所有的代码都可以在 Github 的[上找到。](https://github.com/espressif/esp31-smsemu)

伴随着酷炫的新硬件而来的是一个显而易见的问题:它将于何时发布？这个问题很难回答，但最好的猜测是，“很快”。尽管这种芯片即将问世，但当它发布时，它将为许多项目提供大量的处理能力、WiFi 和蓝牙。它已经入围 2016 年最佳新芯片，但除此之外，没有更多的信息。

 [https://www.youtube.com/embed/HCGHb0OVz1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HCGHb0OVz1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


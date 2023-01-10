# ESP8266 黑仔？

> 原文：<https://hackaday.com/2016/01/30/esp8266-killer/>

我们已经看到 Twitter 上流传着一种新的集成微处理器和 WiFi SOC 的谣言:Nufront 的 [NL6621。细节仍然很少，但这似乎不是因为芯片是蒸汽软件:你现在可以在 Taobao.com](http://www.nufront.com/index.php/portal/page/index/id/366.html)和易贝[购买模块，价格在 2.5 到 3 美元之间，Nufront 的网站上说他们自 2013 年以来已经生产了 100 万个模块。](http://www.ebay.com/sch/i.html?_from=R40&_nkw=nl6621)

NL6621 WiFi SOC 由 160 MHz ARM Cortex-M3 提供支持，具有 448 KB RAM，其他一切都集成在 SOC 中。该模块具有 32 个 GPIOs、SPI、I2C、I2S 数字音频和大多数您期望的外设。他们说他们有一个完全开源的 SDK，但是我们在任何地方都找不到它的链接。期待下一个新事物的英语论坛已经涌现，他们说他们已经就 SDK 联系了 Nufront，所以如果你感兴趣的话，那可能是一个潜伏的好地方。有了 ARM 内核，用不了多久就会有人让 GCC 研究这些东西。

同样值得注意的是，我们已经在之前[宣布了 ESP8266 杀手，它还没有实现。(最终)来自 Espressif 的社区和官方支持的混合似乎是决定 ESP8266 成功的主要因素，而我们尚未在 NL6621 中看到这一点。所以认真对待题目中的问号，但是如果这被证明是下一件大事，记住你第一次听到它的地方，好吗？](http://hackaday.com/2015/07/13/new-part-day-the-esp8266-killer/)

谢谢[大卫·亨特]的提示！
# Hackaday 奖参赛作品:ESP32 Monster 和快速入门

> 原文：<https://hackaday.com/2017/05/28/esp32-monster-and-getting-started-quickly/>

多产的黑客[kodera2t]正在为仍然较新的 ESP32 WiFi 模块开发他自己的" [ESP32 怪物板](https://hackaday.io/project/21321-esp32-monster-board)"开发板。他的板什么都有:以太网，有机发光二极管，LiPo，甚至 CAN-bus。但是，如果不能对微控制器进行编程来使用外设连接，那么所有外设连接都是毫无价值的。

ESP32 的 Arduino 环境进展得相当不错，但它还没有完全具备运行[kodera2t]所有硬件的功能。为了利用所有这些，他需要使用 Espressif 的 SDK——称为“物联网开发框架”,简称 IDF。在他最新的项目日志中，[kodera2t]详细介绍了让 IDF 在 OSX 上运行和编译所需的一切。(和 Linux 的过程很奇怪的相似。)通读这里的[官方说明](https://github.com/espressif/esp-idf/tree/master/docs/get-started)，如果你想要更多，但我们认为【kodera2t】触及所有高点。

当我们按响[kodera2t]的喇叭时，看看他的老项目——一个硬塞进 SD 卡的 Arduino——或者看他的另一个自我[Toshiro Kodera]严肃地谈论他的日常工作，[工程射频超材料](http://hackaday.com/2017/01/04/toshiro-kodera-electromagnetic-gyrotropes/)。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
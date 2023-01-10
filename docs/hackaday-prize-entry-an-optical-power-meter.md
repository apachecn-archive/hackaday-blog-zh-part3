# Hackaday 奖参赛作品:光功率计

> 原文：<https://hackaday.com/2017/09/14/hackaday-prize-entry-an-optical-power-meter/>

这是一类以建造自己的测试设备而闻名的人群。如果你需要一种编程闪存芯片的方法，不要去买，你可以自己做一个。需要频谱分析仪吗？你可以用覆铜板来建造它。作为他的 Hackaday 奖参赛作品，[oakkar7] [正在建造一个光功率计](https://hackaday.io/project/21599-optical-power-meter-with-sfp-and-ddm-protocol)，它足以完成复杂的光纤工作，但仍然是完全的 DIY。

当你进入不是以字母“RJ”开头的网络和电信连接时，你开始偶然发现 SPF 收发器。这些“小型可插拔”设备是小型模块化收发器，能够处理光纤、千兆以太网和其他稍微奇怪的位管道。当与光纤一起使用时，它们可以测量以 dBm 和瓦特为单位的光功率，并且可以通过 UART 进行调试。

[oakkar]的光功率计使用这些 SPF 收发器，并用一个相当简单的电路连接在一起，该电路由一个 Arduino、几个轻触开关、一个诺基亚 LCD 和一个 FTDI UART 组成。将所有这些结合在一起的关键是用于 SPF 和 DDM(数字诊断监控)的 Arduino 库，使用户能够访问这些收发器中的所有配置位。

虽然电路足够简单，可以在一块 perfboard 上构建，但[oakkar]在这一款上的外壳确实让它出类拔萃。只需一点点激光切割丙烯酸树脂和一些支架，[oakkar]就拥有了一个看起来非常专业的设备，并拥有更高级、更昂贵工具的大部分功能。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
# Hackaday 奖品入口:SD 卡上的安全存储

> 原文：<https://hackaday.com/2017/05/08/hackaday-prize-entry-secure-storage-on-sd-cards/>

这给你出了个难题:你如何安全地将数据从一台有空隙的计算机发送到另一台？通过网络发送是正确的，因为这就是空气间隙的全部意义。sneakernet 天生就不安全，你不应该高估装满磁带的旅行车的安全性。对于他的 Hackaday 奖参赛作品，[Nick Sayer]有一个可能的解决方案。是*夺宝奇兵与毁灭神殿* 里的[桑卡拉石，还是需要两张卡的 USB 读卡器。不管怎样，这都是数据物理安全方面的一个有趣实验。](https://hackaday.io/project/20772-orthrus)

Orthrus 是一种用于两个 SD 卡的安全 RAID USB 存储设备，其背后的想法是将两个 SD 卡配对。使用这两种卡，您可以不受限制地读写该 RAID 驱动器。只有一个，数据是不可恢复的，所以如果分开运输，它们在运输过程中是安全的。

该器件的设计基于 ATXMega32A4U。这很像你对 ATMega 的期望，但它有一个内置的全速 USB 接口和硬件 AES 支持。USB 非常适合将两个 SD 卡作为一个驱动器，AES 端口用于使用存储在每个卡上的密钥存储块中的密钥来加密数据。

对于预期的用例，这是一个很好的设计。只有两个都有，你才能从这些 SD 卡上获取数据。然而，[尼克]很清楚施奈尔定律——任何人都可以设计一个他们自己都无法破解的密码系统。这就是他寻找志愿者来破解 Orthrus 的原因。这是一个有趣的挑战，也是我们希望看到打破的挑战。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
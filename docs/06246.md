# 黑客日奖参赛作品:非常非常强大的伺服系统

> 原文：<https://hackaday.com/2017/06/18/hackaday-prize-entry-very-very-powerful-servos/>

几年前，[patchartrand]决定制造一个机器人手臂。规格很简单:他需要一个至少像人类手臂一样强壮的驱动系统。看了汽车之后，找不到低于 3000 美元的解决方案。这导致了[超伺服](https://hackaday.io/project/21332-ultra-servo)的诞生，它是标准业余伺服的嵌入式版本，提供超过一万盎司英寸的扭矩。

你典型的业余爱好伺服有三个主要组成部分。电子板读取某种信号来控制马达。这个马达被绑在某种齿轮系上，电位计读取轴的绝对位置。这基本上就是超伺服正在做的事情，尽管一切都要大得多。

超伺服中使用的电机是一个非常大的有刷 DC 电机。它连接到一个 160:1 的行星齿轮箱，电子设备围绕四个相当大的 MOSFETs 构建。电子器件围绕 ATmega168 微控制器构建，完整伺服系统的规格包括 12 V 或 24 V 操作、TTL、SPI 和标准 RC 通信、60 RPM 空载速度和 60 ft-lbs 扭矩。

这不是你的标准伺服。这是一块巨大的金属来搬运东西。如果你曾经想要一架遥控塞斯纳，那么*给你*。也就是说，这种大小和功率的伺服系统总是很昂贵，预计每台成本为 750 美元。尽管如此，这比同类产品的数千部要少得多，也是 Hackaday 奖的一大亮点。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
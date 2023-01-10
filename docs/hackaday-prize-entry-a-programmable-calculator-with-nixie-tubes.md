# Hackaday 奖参赛作品:带有谢妮电子管的可编程计算器

> 原文：<https://hackaday.com/2016/05/09/hackaday-prize-entry-a-programmable-calculator-with-nixie-tubes/>

对于[罗伯特]参加黑客日奖，他从一些基本问题开始。有什么比数码管更好的？更多的尼西人。有什么比计算器更好？RPN 计算器。两者结合，你得到了什么？即使以 20 世纪 70 年代的台式计算器标准来看，一个大得离谱的计算器也要消耗大量的能量，并且占据太多的空间。对我们来说听起来不错。

至少在有很多的情况下，Nixies 是棘手的设备。它们只消耗大约 50 毫安的电流，但只有在 150 伏以上时才会亮起。这只有大约 7 瓦，对于 Arduino-heads 来说，建立一个电路来驱动时钟的几个 Nixies 是很容易的。[开几十辆 Nixies 有点难](http://hackaday.com/2016/04/13/powering-a-lot-of-nixie-tubes/)。对于[Robert]的 RPN 计算器，他估计该计算器消耗的功率略低于 50W。

考虑到大量的能源问题，[Robert]将注意力转向了显示板。这将是一个非常令人印象深刻的构建，80 个 IN-12B 管被组织成四个堆叠级别，每个级别 20 个管。显像管将由 Maxim MAX6922 VFD 驱动器控制。这种芯片有一个串行接口，这意味着它相对容易让任何微控制器闪烁这些管。当然，它还有双重功能，可以当时钟用。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)
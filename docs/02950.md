# Hackaday 奖参赛作品:最便宜的逻辑分析仪

> 原文：<https://hackaday.com/2016/07/19/hackaday-prize-entry-the-cheapest-logic-analyzer/>

有成堆的旧 128MB 和 256MB 内存在供应室和零件箱里。为了他的 Hackaday Prize 项目，[sot . Eric]正在将这些过时的 RAM 棒变成有用的东西——一个大而快速的逻辑分析仪。它既便宜又简单，可以在试验板上构建。

如果在奇怪的配置中使用旧的 SDRAM 看起来很熟悉，那么你是对的。该项目基于[Soto . Eric]早期的[AVR 逻辑分析仪项目](http://hackaday.com/2016/03/15/sdram-logic-analyzer-uses-an-avr-and-a-dirty-trick/)，该项目使用慢速 AVR 以每秒 30 兆样本的速度测量 32 个逻辑通道。这种构建的唯一方法是将一个旧的内存棒破解为“自由运行”，自动将数据记录到内存中，然后用 AVR 读取。

该项目通过更快地使用更大的内存棒来扩展早期项目，最终目标是一个 32 位、133 毫秒/秒的逻辑分析仪，它更像是一个外围设备，而不是一个单一的整体项目。有了覆盆子 Pi Zero、一块 RAM 和一些其他的逻辑芯片，这个项目可以变成任何东西，从逻辑分析仪到数据记录器再到示波器。是的，这很奇怪，但是制造这个非常方便的工具的部件可以在任何黑客空间或车间中找到，这使得它成为有事业心的硬件黑客的一个很好的诡计。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)
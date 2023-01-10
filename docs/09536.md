# 一个适用于你的 DOS PC 的并行端口合成器

> 原文：<https://hackaday.com/2018/05/22/a-parallel-port-synthesiser-for-your-dos-pc/>

非常遗憾的是，在过去，一台典型的家用计算机拥有简单的低级硬件访问功能，而今天的计算机却没有这种功能，利用这种功能的成本非常高。专业的 PCB 对于家庭建筑商来说是遥不可及的，并且许多可能已经使用的集成电路是昂贵的并且难以小批量采购。

在 21 世纪，我们既有廉价的印刷电路板，又能方便地获得大量的半导体，因此对旧硬件的爱好者可以着手进行以前不可能完成的项目。这样的产品是[Serdef]的用于 DOS PCs 的微型并行端口通用 MIDI 合成器,这是一款非常专业的合成器，三十年前你可能会花很多钱去拥有它。

其核心是一个 SAM2695 合成器芯片，该板使用并行端口作为 8 位 I/O 端口。软件方面由一个 TSR(一个在启动时加载的[终止并保持驻留的](https://en.wikipedia.org/wiki/Terminate_and_stay_resident_program)驱动程序，对于那些不是 DOS 爱好者的人来说)处理，并且有几个经典游戏的运行演示。

如果你对这里使用的芯片感兴趣，你可能会想看看类似的 Arduino 项目。我们讨论过的 Kickstarter 现在已经结束了，但是[你也可以在 GitHub](https://github.com/brainmux/AvecSynth) 上找到它。
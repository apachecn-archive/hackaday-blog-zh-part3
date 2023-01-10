# Hackaday 奖参赛作品:机器狗学会跟随

> 原文：<https://hackaday.com/2017/08/13/hackaday-prize-entry-robo-dog-learns-to-heel/>

[Radu Motisan]正在研究一种小型漫游车，它的主要技巧是能够识别它的主人。Robo-Dog 是他的概念证明，它是一辆使用五个超声波传感器向最近的障碍物移动的漫游车。很明显，这并不等同于能够把一个人和另一个人区分开来，但这是一个开始。

这些传感器是使用焊接在定制电路板上的超声波胶囊自制的，管状外壳由 PVC 管制成。他制作了一个超声波信标，使用 556 定时器 ic 来发射 40 千赫的脉冲，这样他就可以完全用声音来控制机器人。如果失败了，机器狗前面还有一个红外接近传感器。所有这些都由 ATmega128 板和定制的 H 桥电机控制器控制。

[Radu]一直在微调算法，使机器狗移动得更快以赶上远处的目标，但对近处的目标移动得更慢。它比较两个传感器的读数来计算接近角。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
# 测量电容与电压的关系

> 原文：<https://hackaday.com/2015/12/11/measuring-capacitance-against-voltage/>

陶瓷电容几乎是电子世界的精灵尘。如果你在电路上洒上足够多的这种物质，一切都会正常。然而，这些陶瓷电容器并不是最新的技术:你可以在 20 世纪 30 年代的收音机中找到它们，它们有一个令人讨厌的特性:它们的电容随电压而变化。

如果你依赖 RC 滤波器或电源中的陶瓷电容，这是一个问题。你需要的是一个能够绘制电容与电压关系图的设备，而[limpkin] [将向你展示如何做到这一点](http://www.limpkin.fr/index.php?post/2015/11/24/An-Open-CVMeter)。

当然，电容通常是通过计时电容通过 RC 振荡器充放电的时间来测量的。这需要至少一个已知值，本例中为 0.1%电阻，通过测量该电路振荡所需的时间，可以计算出未知电容。

这很好，但如何测量偏置电压下的电容呢？ [EDN 用一个围绕运算放大器构建的简单电路扭转了局面](http://www.edn.com/design/power-management/4438321/How-to-measure-capacity-versus-bias-voltage-on-MLCCs)。该运算放大器只是一个比较器，电路的其余部分提供与电容电荷百分比成正比的电压。

这个小项目[limpkin]已经变成了 Kickstarter，也是我们[在](http://hackaday.com/2015/11/14/measuring-capacitors-over-their-working-voltage/)之前见过的[。也就是说，测量电容与电压的关系不是任何一种电表能做到的，我们很高兴[limpkin]能开发出一种简单易用的工具来测量这种现象。](http://hackaday.com/2015/11/14/measuring-capacitors-over-their-working-voltage/)
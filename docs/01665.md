# 将电动滑板车换成锂电池并禁用安全装置

> 原文：<https://hackaday.com/2016/03/02/converting-an-electric-scooter-to-lithium-batteries-and-disabling-safeties/>

现在有很多不同的电动滑板车，包括那些不断着火的悬浮滑板。[TK]有一个使用铅酸电池的旧剃须刀 E300。在厌倦了低速和 12 小时的充电时间后，[TK]决定是时候[换成锂电池](https://hackaday.io/post/32983)了。

新电池来自一台 Ryobi 钻机。每个提供 18 V，串联提供 36 V。原来的电池只能在 24 V 下运行，这导致了电机控制器的一些问题。它拒绝用更高的电压启动。解决方案:用一根电线桥接电机控制器上的安全关闭继电器，使其失效。

随着电压问题的解决，是时候修改电流限制了。该电机控制器使用 TI [TL494](http://www.ti.com/product/TL494) 产生 PWM 波形，驱动 MOSFET 为电机提供可变功率。切断 TL494 电流检测引脚的走线，可以完全消除电流限制。

我们并不是说禁用你的踏板车上的所有电流和电压限制是明智的，但它似乎对[TK]有效。这款售价 200 美元的踏板车现在的时速从 22 公里提高到了 28 公里，充电速度也快了很多。有了传动装置，他希望能有更多的表现。

休息过后，全转换视频。

 [https://www.youtube.com/embed/PQLBgA0a7t8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PQLBgA0a7t8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


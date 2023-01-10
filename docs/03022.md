# Hackaday 奖参赛作品:压电步态分析

> 原文：<https://hackaday.com/2016/07/22/hackaday-prize-entry-piezo-gait-analysis/>

走进一家高档药店，你可能会发现你所见过的最令人惊叹的销售演示。走上前去，脱掉鞋子，把你的脚放在神奇的舒尔博士的机器上，你会得到一个定制的读数，显示你的脚是如何接触地面的。作为额外的奖励，你还会得到一个鞋子衬垫的推荐，它会让你的脚感觉更好，你的鞋子也更合脚。

当然，这种设置有一个问题。你不会整天站在足迹测量仪上。测量你的脚如何着地的问题的一个更好的解决方法是在你走路的时候做。这就是[【芯片机器人】的 Alli-Gait-Or 分析的用武之地](https://hackaday.io/project/11154-alli-gait-or-analysis)。那是舒尔博士藏在鞋底的机器。它可以在你走路的时候穿，它可以准确地告诉你你的脚是如何工作的。

[chiprobot]的机器人鞋由一个 3D 打印插件组成，每只鞋可以容纳 18 个压电传感器。这些连接到 ADC，ADC 输入微控制器，微控制器将数据发送到计算机。这很简单，但是理解这些数据才是真正的问题。

为了将这些数据转化为可以用于选择矫正器或简单地找到更好的鞋子的东西，[chiprobot]正在将这些数据插入 Blender [并创建一些非常酷的可视化效果](https://hackaday.io/project/11154/log/41174-blendering-a-display-gui)。从鞋子上获取一些重要的数据已经足够好了，因为这种 Alli-Gait-Or 是可穿戴的，所以这些数据比坐在药店里的机器更有效。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)
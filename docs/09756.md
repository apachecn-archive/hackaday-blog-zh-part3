# Hexabitz，模块化电子产品变得更简单

> 原文：<https://hackaday.com/2018/06/20/hexabitz-modular-electronics-made-easier/>

多年来，已经出现了多种模块化电子系统，这些系统允许通过包含单独功能的模块的互连来创建复杂电路。Hexabitz，一种互锁的多边形小型 PCB，就是这样一个系统。它能带来什么别人还没有做过的事情？

模块化电子设备的设计者面临的问题是:所有设备都有不同的要求和接口。为了允许模块之间的连接并保持所有这些连接，需要模块间连接器的复杂性不断增加，或者对该问题应用一点智能。Hexabitz 的设计者选择了后一种角度，为每个模块配备一个 STM32 微控制器，使其能够识别自身及其功能，并与同一连接项目中的其他模块建立网状网络。这也使系统能够将计算任务分配给各个模块，而不是仅仅依赖于单个微控制器或单板计算机。

该系统可以拥有极其全面的模块阵列,这为其提供了一些有趣的可能性，然而，它受到模块化电子系统的固有问题的困扰，即不太容易合并非标准功能。如果他们能够破解一个原型模块，并通过一种简单的方法告诉其微控制器识别其上的功能，他们可能会有一个赢家。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)
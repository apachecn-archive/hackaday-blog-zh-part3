# 电磁驱动的钟摆

> 原文：<https://hackaday.com/2017/12/30/electromagnet-powered-pendulum/>

我们总是很高兴看到黑客们被他们在 Hackaday 上看到的东西激励着去尝试不同的东西。To [SimpleTronic]有一个项目可以让你以一种非常有趣的方式拓展你的模拟电子技能。是一个[电磁铁摆模拟电路](https://hackaday.io/project/28602-magnetic-pendulum)。无论你是在建造它，还是只是在研究原理图，这都是一种有趣的方式来温习工艺的非数字方面。

钟摆是一个螺栓头上的钕磁铁，悬挂在一英尺长的铝链上。下图中，一个霍尔效应传感器位于一个直径为 1 英寸的电磁体上，6/8 英寸的电线缠绕在另一个螺栓上。当摆锤的磁铁向电磁铁的核心加速时，霍尔效应传感器记录到电压的增加。当钟摆经过头顶时，电压达到峰值，一旦霍尔效应传感器检测到电压下降，电磁铁就会开启一会儿，将钟摆推开。该电路功耗非常低，因为电磁体仅开启约 20 毫秒！

其他主要元件包括一个 LM358N 运算放大器、一个 CD4001B 四通道 CMOS 或非门和 IRFD-120 MOSFET。[SimpleTronic]甚至花时间突出原理图的每个部分，以便完成完整的解释。

 [https://www.youtube.com/embed/_b4tsJTQzD8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_b4tsJTQzD8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



最后，这个模拟电路应该可以帮助新人熟悉电磁体，这样他们就可以进入下一个逻辑步骤:[线圈枪](https://hackaday.com/2016/08/19/coil-gun-for-newbies-learning-electromagnetic-propulsion/)和[网射器](https://hackaday.com/2014/04/22/electromagnetic-spiderman-webshooter-railgun-grappling-hook/)。

[通过 T0 黑客攻击。io]t1
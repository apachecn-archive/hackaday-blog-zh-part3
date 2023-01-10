# 洪水故障断路器可以拯救生命

> 原文：<https://hackaday.com/2018/05/16/flood-fault-circuit-interrupter-could-save-lives/>

如果你不必冒着生命危险在灾难性的暴风雨中切断电源会怎么样？这是休斯顿的许多人在看到飓风哈维和其他风暴带来的水在街道上涌动，在排水沟中膨胀，淹没他们的家园时问自己的问题。

这些休斯顿人当中有工程系的学生[乔恩]和[赛勒斯·杰扬]。他们看着房主奋力将他们的房子与电网安全断开，并说，事情不应该是这样的。[他们](https://hackaday.io/project/153872-flood-fault-circuit-interrupter) [设计了洪水故障断路器来监控目标区域，并在检测到可信威胁时自动切断电源](https://hackaday.io/project/153872-flood-fault-circuit-interrupter)。

FFCI 建立在现有的保护方案之上，如 GFCIs 和电弧故障断路器。这并不意味着取代它们，而是将它们联系在一起，并根据浮控开关的输入关闭它们。

随着洪水上涨，EEPROM 进行查找和比较，以确定威胁是否足以关闭它。如果是这样的话，发送到并联跳闸断路器的警报信号可以将整个系统关闭，或者切换到备用电源。该系统围绕支持 12 V 报警输出的标准安全面板和键盘接口构建。我们特别喜欢浮动开关外壳，它允许水进入，同时防止碎片进入。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)
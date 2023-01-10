# 带激光成像的激光印刷电路板

> 原文：<https://hackaday.com/2017/06/15/laser-pcbs-with-ldgraphy/>

有很多很多方法可以将 PCB 设计放到电路板上进行蚀刻。然而，即使在实践中，结果的质量也随着所使用的工艺和设备而变化。随着 QFN 部件成为标准，蚀刻抗蚀剂转移和永久标记的日子几乎一去不复返了。幸运的是，由于世界各地的黑客，近年来已经设计出了新的和改进的 Gerber 转移方法。

其中一名黑客[Henner]正致力于一个名为[LDGraphy](https://github.com/hzeller/ldgraphy)的项目，试图将高分辨率蚀刻技术带给大众。LDGraphy 是一种激光光刻设备，它利用激光和猎兔犬骨绿将布局蚀刻到电路板上。最好的部分是，整个 BOM 被称为成本低于 100 美元，使人们能够负担得起的预算。

该系统是围绕一个 500 mW 的激光器和一个用于激光打印机的多面镜扫描仪设计的。使用步进电机在 X 轴上线性驱动具有光致抗蚀剂的板，并且从旋转的六边形反射镜反射的激光束负责 Y 轴。AM335X 处理器的可编程实时单元(PRU)的时间关键代码以汇编形式编写，用于快速激光切换。外壳自然是一个激光切割的丙烯酸外壳，在[Henner]当地的 hackerspace 制造。

[Henner]一直在努力校准他的设计，并补偿所用组件的不准确性。在下面的演示视频中，他展示了一个分辨率为 6 密耳的工作版本，考虑到机器的成本，这是非常好的。如果你想帮忙，他还会在 GitHub 上分享他的代码，你也可以在 T2 的 Google+(T3)上跟踪他的更新。

这不是我们第一次看到 [DIY 激光 PCB 曝光机](http://hackaday.com/2012/08/09/exposing-pcbs-with-a-home-made-laser-printer/)，当然，这是最好的记录之一。如果你在寻找其他方法来弄脏你的衣服，那么[真空曝光](http://hackaday.com/2016/09/18/vacuum-exposure-unit-gives-better-pcb-etching-results/)或者一些[蚀刻技术教程怎么样？](http://hackaday.com/2013/03/04/frans-pcb-etching-techniques/)

 [https://www.youtube.com/embed/G9-JK2Nc7w0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G9-JK2Nc7w0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


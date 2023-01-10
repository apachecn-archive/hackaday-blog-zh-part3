# 理解浮点数

> 原文：<https://hackaday.com/2017/10/02/understanding-floating-point-numbers/>

人们以不同的方式学习，但有时机构专注于用一种方式解释一个概念。如果这不是你的方式，你可能就不走运了。如果你在内化浮点数表示方面有困难，互联网是你的朋友。【Fabian Sanglard】(游戏引擎黑皮书作者:Wolfenstein 3D)不喜欢浮点数的传统表示方式，所以他决定[用一种不同的方式](http://fabiensanglard.net/floating_point_visually_explained/)来解释它们。

[Fabian]没有像传统术语那样考虑指数和尾数，而是将指数称为一个“窗口”,它决定了数字在 2 的 2 次方之间的范围。所以窗口可以是从 1 到 2，或者从 1 024 到 2048，或者从 32768 到 65536。

一旦确定了窗口，尾数(Fabian 称之为偏移量)将窗口范围分成 8，388，608 个部分，假设是 32 位浮点型。就像 8 位 PWM 值使用 128 表示 50%一样，如果值在窗口的中间，偏移(或尾数)将是 4，194，304。

有一些细节被掩盖了——指数的偏差和尾数中的假设数字在提供的公式中，但它们的原因没有像“经典”解释那样清楚地说明。如果你想尝试传统的课堂讲座，下面有一个。

我们已经讨论了浮点表示法及其对导弹的影响。曾经有一段时间，你讨厌使用浮点运算，因为无论是从成本还是 CPU 时间来看，它都非常昂贵，但是[现在，即使是焊接控制器也可以用浮点运算进行相对快速的运算](https://hackaday.com/2017/03/08/one-soldering-controller-to-rule-them-all/)。

 [https://www.youtube.com/embed/ji3SfClm8TU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ji3SfClm8TU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


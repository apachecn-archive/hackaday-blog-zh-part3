# 终于来了！一个银杜伊诺！

> 原文：<https://hackaday.com/2016/03/05/at-last-a-sil-duino/>

有一些标准组件一直在不断改进，即使不完美，也已经变得尽善尽美。以 Arduino Uno 为例，将其与十年前的祖先进行比较。它们表面上是同一个主板，彼此兼容，但 Uno 及其现代克隆产品具有更高的处理能力、内存和存储能力，USB 接口而不是串行接口，以及一系列小组件变化，使它们更好、更便宜。

你可能会认为，另一个 Arduino 克隆体当时不会带来太多东西。从广义上说，你是对的，还有什么需要改进的呢？

[Clovis Fritzen]有一个值得再看一眼的 Arduino 克隆体的想法。这不是一个会让 Arduino 世界火起来的惊人的硬件模块，而是一个非常简单的设计特征。他创造了一个垂直安装在单排插销上的 Arduino。你可能会问，为什么你会觉得这很有吸引力？SIL 垂直 Arduino 比现有的 DIL Arduinos 占用更少的试验板空间。这是一个简单的想法，但是如果你发现自己没有面包板了，这个想法会非常有用。

[Clovis]采用 Arduino Uno 的电路，并通过移除 USB 接口来简化它，因此该板必须通过其 ICSP 接头进行编程。他把它做成一个通孔板，便于那些担心 SMD 焊接的人建造。生成的板卡文件[都可以在 GitHub](https://github.com/FritzenLab/Fritzen_Proto-controller) 上找到。

时不时会出现一个如此简单、显而易见且有用的方法，以至于你想知道为什么你自己没有想到它。我们中的许多人都会使用 DIL Arduino，并且可能会发现自己耗尽了试验板空间。这种主板可能不会改变世界，但它至少可以让我们中一些摆弄微控制器的人的生活变得更加轻松。

这只是众多 Arduino 克隆版本中最新的一个。2013 年，我们问为什么当[展示一个 PCB 设计练习](http://hackaday.com/2013/09/03/another-arduino-clone-is-the-last-thing-the-world-needs/)时，世界需要更多。甚至还有由布莱恩·本切夫开发的名为 HaDuino 的黑客版本[。但是，虽然另一个普通的 Arduino 克隆产品确实没有带来任何东西，但这不应该阻止人们使用 Arduino 并对其进行黑客攻击。每隔一段时间，像这个项目这样有用的东西就会从中产生，这对我们的社区来说只会是一个好处。](http://hackaday.com/2013/10/11/haduino-open-your-beer-using-arduino/)
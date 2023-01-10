# 绑定更多闪存

> 原文：<https://hackaday.com/2017/09/10/bodging-on-more-flash-memory/>

[Curmudegeoclast]发现自己在一个小 M0 板上的闪存快用完了，所以他决定在原来的 CPU 上[环氧树脂和飞线连接一个巨大的 2 MB 额外闪存。](https://daveastels.com/2017/09/01/trinket-m0-express-hack/)

我们将让我们的“这些天的孩子”咆哮的方式了:股票 SAMD21 ARM 芯片有 256 kB(！)的闪存，位于一个只有五个 GPIO 引脚的分线板上，每引脚比率为 51 kB！现在他又增加了 2 MB？这太疯狂了。[Curmudegeoclast]这么做的原因是 MicroPython，它占用了 flash 的很大一部分，仅仅是基础语言。我们怀疑也有相当数量的“这不是很好吗？”混合在一起。随便啦。

黑客是经典。它从焊接到引脚的粗导线开始，并用 SOIC 扩展板进行试验。在概念验证之后，通过将闪存芯片 dead-bug 粘合在微控制器顶部，将某种程度的结构完整性带入程序中。我们爱这个(0805？)也是点对点焊接到位的 SPI 上拉电阻。为了“长期”稳定，我们无法抵制将整个事情埋葬在热胶水中的诱惑，但是也有更好的选择。

这个黑客拿了一个极简主义的板子，然后加大了尺寸，为此，值得称赞。在一个小小的微控制器上，你会在 2 MB 的免费闪存中放入什么？你们中使用 MicroPython 或 CircuitPython 的人介意对闪存需求发表评论吗？256 kB 对任何人来说应该都够了。
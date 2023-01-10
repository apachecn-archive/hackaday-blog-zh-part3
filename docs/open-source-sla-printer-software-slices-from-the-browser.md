# 从浏览器中开放源代码 SLA 打印机软件切片

> 原文：<https://hackaday.com/2016/06/13/open-source-sla-printer-software-slices-from-the-browser/>

基于树脂的 SLA 打印机需要与“普通”熔融塑料打印机不同的切片算法。在他们最近的黑客马拉松之后，来自 Formlabs 的[Matt Keeter]和[Martin Galese]完成了一个开源切片器，这个可以在你的浏览器上运行。这是 Javascript，所以你可以在他们的网页上测试一下。

对于 SLA 打印机来说，弄清楚每一层的体素是在模型内部还是外部更加困难，因为它们必须明确考虑模型内部的内部“空白”空间。[Matt]和[Martin]的软件在切片时会计算出这个值。为了做到这一点，[Matt]设计了一个聪明的算法，它利用现有的硬件在切片过程中快速积累体素的内外状态。

[Matt]对 3D 网格操作和黑客技术都不陌生。如果你刚刚开始进入这个领域，看看[锑](http://hackaday.com/2015/05/29/otherworldy-cad-software-hails-from-a-parallel-universe/)，【马特】超凡脱俗的 CAD 软件，它有一个 Python 界面，让你体验一下参数化 3D 建模。
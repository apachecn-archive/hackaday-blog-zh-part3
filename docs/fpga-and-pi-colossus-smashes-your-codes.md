# FPGA 和 Pi 巨像粉碎你的代码！

> 原文：<https://hackaday.com/2016/06/08/fpga-and-pi-colossus-smashes-your-codes/>

如果是在 60 年前，你试图保守秘密，你会很高兴[Ben North]没有带着他的[Raspberry-Pi-and-FPGA 密码破译机](http://bennorth.github.io/fpga-colossus/doc/Content/notes.html)回到过去。

我们已经在 Hackaday 看到了很多英格玛的版本——二战时期的加密机器激发了我们读者的想象力。但是也许在那个时代密码分析中出现的更重要的机器是图灵的机电炸弹，因为它破解了英格玛密码，以及基于真空管的 T2 巨像，因为它是第一批可编程电子数字计算机之一。

[Ben]的构建将他对老式密码分析的探索与 FPGAs 的实际学习项目结合起来。如果你对以上任何一个感兴趣，看看吧。你可以从他对 Colossus 的 [Python 实现开始，然后进入他的](http://redfrontdoor.org/Dickens-Teleprinter/index.html) [GitHub 库](https://github.com/bennorth/fpga-colossus/tree/published)，了解 FPGA 的本质。

这也是一个使用 [XuLA2 FPGA 板](http://www.xess.com/shop/product/xula2-lx25/)及其同伴 StickIt 板的很好的例子，它们直接插入 Raspberry Pi 进行编程和支持。自从 2012 年我们[第一次听说它们以来，我们还没有看到很多项目使用它们。然而，这个](http://hackaday.com/2012/12/11/breadboard-friendly-fpgas/)[虚拟男孩黑客](http://hackaday.com/2013/06/17/giving-the-virtualboy-a-vga-out/)引起了我们的注意。它看起来像一个不错的平台。还有人在用吗？
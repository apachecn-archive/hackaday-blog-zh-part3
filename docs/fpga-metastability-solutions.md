# FPGA 亚稳态解决方案

> 原文：<https://hackaday.com/2017/10/25/fpga-metastability-solutions/>

Gisselquist Technology 最近发布了一篇关于亚稳态和常见解决方案的博客文章。如果你正试图学习 FPGAs，你会想要阅读它。如果你已经对 FPGAs 有了很多了解，你可能还会在文章中发现一些有趣的花絮。

不要让亚稳定性这个词吓到你。这只是一种奇特的说法，即如果输入在时钟沿之前的一定时间内不稳定，而在时钟沿之后的一定时间内保持稳定，则触发器会变得疯狂。这些时间分别是建立时间和保持时间。

通常，如果使用单时钟，设计工具会警告您可能出现的问题。然而，任何时候您的设计用一个时钟产生一个信号，然后用另一个时钟在某个地方使用它，亚稳态都是一个可能的问题。即使您只有一个时钟，任何不参考您的时钟的外部输入，或者任何时钟，都有可能导致亚稳态。

更糟糕的是，一个设计可以在大部分时间工作，只是偶尔会违反设置或保持规则。例如，连接到按钮的输入可能十次有九次工作正常，但在第十次时，按钮的按下恰好与时钟边沿同步。人字拖会有什么作用？它可以采用一个既不是零也不是一的水平，或者它可以来回振荡。

我们会让你自己阅读解决方案。然而，如果你想听听我们的看法，我们已经讨论过[亚稳态](https://hackaday.com/2015/09/24/learn-flip-flops-with-more-simulation/)作为触发器系列的一部分。你也可以看看下面关于现实生活的视频。如果你想了解更多关于人字拖的基础知识，你可能想从该系列的[第一帖](https://hackaday.com/2015/09/23/learn-flip-flops-with-simulation/)开始。

 [https://www.youtube.com/embed/alRaqQzTPds?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/alRaqQzTPds?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


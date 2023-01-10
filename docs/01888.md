# 窥视 GPU 黑匣子内部

> 原文：<https://hackaday.com/2016/03/30/peering-inside-the-gpu-black-box/>

宾厄姆顿大学的研究人员已经建立了他们自己的图形处理器单元，可以被闪存到 FGPA 中。虽然“图形”是其名称，但这种 GPU 设计旨在提供一种通用计算外设，即 GPGPU 测试床。当然，这并不意味着你不能[在上面玩《雷神之锤》(慢)](http://latchup.blogspot.com/2015/06/not-so-fast.html)。

宾汉姆顿船员的设计不仅是开放的，而且很容易修改。这是一个 GPGPU，你不仅知道芯片内部发生了什么，还拥有开源驱动程序和接口。正如蒂莫西·米勒教授所说，

> GPU 制造商都决定对他们的芯片规格保密，这对开源社区是不利的。这阻止了开源开发者编写可以利用该硬件的软件。有了“开放硬件”社区的贡献，我们可以整合更多的创意，开发出越来越好的工具。

这就是你进来的地方。团队成员之一的[Jeff Bush]有一个很棒的博客，上面有一个关于已知 GPU 设计的详细介绍。所有的 Verilog 和 C++代码都在[【杰夫】的 GitHub](https://github.com/jbush001/NyuziProcessor) 上，包括[的文档。](https://github.com/jbush001/NyuziProcessor/wiki)

如果你对 GPU 内部的深层魔力感兴趣，这里有一个窥探黑盒内部的好方法。
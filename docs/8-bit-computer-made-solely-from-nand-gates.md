# 仅由与非门制成的 8 位计算机

> 原文：<https://hackaday.com/2016/02/24/8-bit-computer-made-solely-from-nand-gates/>

作为一名电子学新手，当他们教你逻辑门时，首先告诉你的一件事是，“你可以用与非门的组合制造任何东西”。接下来通常会演示由与非门构成的简单的“与”、“或”和“异或”门，可能还会有一两个触发器。然后你继续前进，当你需要一个逻辑功能时，你使用包含它的相关设备，关于与非门的金块信息就变成了你电子学常识的一部分。

但不是亚历山大·沙巴欣。他给自己设定的任务是[完全从与非门](https://hackaday.io/project/9795-nedonand-homebrew-computer)中创建一个完整的 CPU，并且他正在使用 74F00 芯片来提供所希望的 1 兆位性能。他的设计有 8 位数据总线，但有 4 位 ALU，以及令人印象深刻的 2 级流水线和 RISC 指令集，这使它与我们大多数人拥有的计算机不同，当时 74 系列逻辑是一项更近的创新。到目前为止，他已经完成了一个 D 型触发器和一个一位运算器的印刷电路板，其中四个将在最终的机器中并行工作

不出所料，我们在 Hackaday 对 TTL 计算机保持浓厚兴趣已经有很长时间了。你可能会说，我们已经为这个主题精选了这么多，值得一篇自己的评论文章。有 [ASAP-3](http://hackaday.com/2013/11/04/asap-3-the-almost-simple-as-possible-computer/) 、 [Magic-1](http://hackaday.com/2011/07/18/building-a-computer-around-a-ttl-cpu/) 、 [Duo Basic](http://hackaday.com/2013/11/03/duo-basic-an-all-logic-chip-educational-computer/) 、 [Apollo181](http://hackaday.com/2012/05/15/building-a-4-bit-ttl-computer/) 、【唐恩·斯图尔特】制造的[无名 CPU](http://hackaday.com/2009/10/30/processor-built-with-transistor-transistor-logic/) 、 [BMOW](http://hackaday.com/2009/02/27/bmow-a-home-made-cpu/) 以及阿波罗制导计算机的一个[克隆体](http://hackaday.com/2008/08/31/apollo-guidance-computer-clone/)。但让[亚历山大的]项目与所有这些优秀机器不同的是他的裸机和纯 NAND 设计。其他 74 系列 CPU 设计者已经拥有了诸如 [74181 ALU](https://en.wikipedia.org/wiki/74181) 之类的全系列器件。通过在这个最基本的层次上研究构建模块，可以更深入地理解通常被表示为黑盒的部件的内部工作原理。

写黑客文章的一个要点是，如果主题让作者停下来阅读而不是浏览，那么读者也可能会这样做。这个项目可能还没有交付一个工作的 CPU，但它迄今为止的进展足够有趣，值得深入阅读。绝对值得一看。
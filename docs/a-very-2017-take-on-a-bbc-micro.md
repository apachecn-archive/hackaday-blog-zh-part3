# 一部非常 2017 年的 BBC 微电影

> 原文：<https://hackaday.com/2017/09/24/a-very-2017-take-on-a-bbc-micro/>

在 20 世纪 80 年代初，市场上有过多的 8 位微型计算机，如果你对这些东西感兴趣，你可能属于某个特定制造商产品的不同爱好者群体之一。如果你是英国人，那么很可能有一种机器会为那个时代所有机器的拥有者提供一个共同的参照系:Acorn BBC 微型计算机，它在英国的学校里无处不在。今天，这台 6502 驱动的机器被认为是第一代 ARM 处理器的祖先和主机，但在当时，它因包含大量内置接口而闻名。它相对较高的价格意味着说服你的父母给你买一个而不是一个 ZX 频谱将永远是一场艰苦的斗争。

所以，你从未拥有过 BBC 的微型摄像机，这给你留下了终生的创伤。没关系，一切都没有失去，因为现在你可以在 myStorm FPGA 板上完全以硅芯片运行一个经典的微处理器，而不用在易贝到处寻找。

公平地说，在 FPGA 上运行经典硬件并不是什么新鲜事，已经有一些 BBC Micros 以这种方式实现，[更不用说 Acorn Atom](https://hackaday.com/2017/08/28/retrocomputing-with-open-source-fpgas/) 了。但这个项目建立在以前的 FPGA BBC Micros 之上，将它完全移植到 Verilog，并结合了来自各个分支的一些错误修复。有运行几个经典游戏的结果截图，以及测试屏幕和基准测试，显示它是 2MHz BBC Micro 的忠实再现。

去年 myStorm board 上市时，我们报道了它。我们还为你带来了[另一个 FPGA 板，作为一个真正的 BBC 微](https://hackaday.com/2015/10/03/vintage-bbc-computer-gets-fpga-buddies/)的协处理器运行。

谢谢你的提示。他还提醒我们，myStorm 板的 ARM 微控制器[现在可以通过 Arduino IDE](https://forum.mystorm.uk/t/blackice-and-arduino/265) 进行编程。
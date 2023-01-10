# 虚拟 CPU 保留在脚本中

> 原文：<https://hackaday.com/2017/07/22/virtual-cpu-stays-on-script/>

有些人会认为这是一件伟大的事情，而其他人则认为这是 JavaScript 每天被滥用的一个例子，但[Francis Stokes]决定设计自己的 CPU 架构，并使用 JavaScript 实现了它的虚拟版本[。CPU 是一个 16 位事务，有一个简化的汇编语言。代码在](https://francisstokes.wordpress.com/2017/07/20/16-bit-vm-in-javascript/) [GitHub](https://github.com/francisrstokes/16bitjs) 上，但真正的价值是【Francis 的】在原帖中对设计的阐述。

在讨论设计时，[Francis]展示了他对指令集的第一次检查，讨论了他发现的错误，然后展示了由真实指令和一些宏组成的最终集，以处理其他常见情况。

[Francis]看[Ben Eater]的[视频](https://hackaday.com/2017/04/10/8-bit-breadboard-computer-is-up-to-8-hours/)得了 CPU bug。当然，[本的]中央处理器是 8 位的，并生活在一个试验板上。如果我们想要测试一个新的指令集架构，我们可能会使用 C 或 C++或者……嗯，老实说，除了 JavaScript 之外的任何东西。但如果说我们学到了什么的话，那就是每个人的品味都不一样。不过，我们毫不怀疑，双方都会有一些激烈的评论。

如今，为运动开发 CPU 已经变得非常流行。当然，很少有人有 [A2Z](https://hackaday.com/2017/01/13/fpga-computer-covers-a-to-z/) 那样的周边环境。
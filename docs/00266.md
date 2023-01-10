# 老式英国广播公司计算机获得 FPGA 好友

> 原文：<https://hackaday.com/2015/10/03/vintage-bbc-computer-gets-fpga-buddies/>

BBC 微型计算机系统(或 BBC Micro)是 20 世纪 80 年代早期的一种创新机器。给评论家留下深刻印象的一个特征是“管道”接口，它允许机器成为附加 CPU 的 I/O 处理器。当板载 6502 变得太慢时，它可能会成为 Z-80 甚至 ARM 处理器的奴隶。总线实际上对任何高速设备都有用，但它的目的是添加新的处理器，这是一个名为“创新”的功能字节杂志

[Hoglet67]发布了一组非常有趣的 FPGA 设计，允许搭载 Xilinx Spartan 3 的小型电路板通过 tube 接口将 6502、Z80、6809 或 PDP/11 添加到 BBC Micro。经典计算机充当实现更老 PDP/11 的相当现代的 FPGA 的 I/O 奴隶，这是令人满意的。

这个项目有一组冗长的线程，但最容易开始的地方可能是这个探路者线程。你可能也想[了解更多关于管接口](https://en.wikipedia.org/wiki/Tube_(BBC_Micro))的信息。在下面的视频中还有对 BBC Micro 的一位设计师的采访。

在我们最近对经典计算机模拟器的综述中，我们忽略了 BBC Micro，但是 PKM 提供了一个链接。如果你身边没有 BBC 的微处理器，也许[只需在 FPGA 上运行整个 6502 计算机就可以了](http://hackaday.com/2014/08/16/an-fpga-based-6502-computer/)。也许你甚至可以给它添加你自己版本的管道接口。

 [https://www.youtube.com/embed/y4WG549i3YY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/y4WG549i3YY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Ed S]的提示！
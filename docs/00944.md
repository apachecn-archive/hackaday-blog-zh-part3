# 从 PLC 读取智能卡(在 Arduino 的帮助下)

> 原文：<https://hackaday.com/2015/12/18/reading-smart-cards-from-a-plc-with-a-little-arduino-help/>

如果你在工厂或车间待过一段时间，那么你很可能遇到过 PLC(可编程逻辑控制器)。这些都是坚固的计算机，做简单的控制和监测功能，通常使用梯形逻辑来设置他们的程序。[plc4u]想要将智能卡读卡器连接到 Allen Bradley PLC，所以他转向使用 Arduino 作为中间人。

Arduino 使用 USB 主机保护罩与 USB 读卡器对话。然后，它使用 RS232 链路和大多数 Allen Bradley PLCs 理解的 [DF1 协议](https://en.wikipedia.org/wiki/DF-1_Protocol)与 PLC 通信。您可能不需要智能卡，但一旦您知道如何在 Arduino 和 PLC 之间进行通信，您就可以做许多不同的项目，利用 Arduino 上可用的其他 I/O 设备和代码，并连接到现有的 PLC 安装。请记住，您可能需要对 Arduino 进行一些加固，以确保其安全，达到与 PLC 相同的水平(可能包括 NEMA 外壳，甚至防爆箱)。

我们之前已经覆盖了[多个](http://hackaday.com/2012/10/27/openplc-for-industrial-automation-to-halloween-displays/)T2【开源 PLC 项目。如果你想了解更多关于 PLC 使用的梯形逻辑，有一个关于这个主题的视频[。然而，下面的视频显示了智能卡阅读器的运行。](https://www.youtube.com/watch?v=Ei4_HqzUFBs)

 [https://www.youtube.com/embed/zqRv2GA_nqk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zqRv2GA_nqk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



PLC 图片:由 Cmarcante(自己的作品)[ [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0) ]，通过维基共享
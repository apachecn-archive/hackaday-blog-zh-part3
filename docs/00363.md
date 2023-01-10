# 与 Zynq 一起高飞

> 原文：<https://hackaday.com/2015/10/14/flying-high-with-zynq/>

【Aerotenna】最近宣布[由运行 ArduPilot](http://aerotenna.com/uav-flight-with-zynq-processor/) 的 Xilinx Zynq 处理器驱动的无人驾驶飞行器(UAV)首次成功飞行。Zynq 是一款带有板载 FPGA 的双臂处理器，可以卸载处理器或提供定制 I/O 设备。他们计划将他们的代码发布到他们的 [OcPoC(芯片上的八角形飞行员)项目](http://aerotenna.com/open-source-micro-pilot-system/)，这是一个开源项目，与开源无人机平台 [Dronecode](https://www.dronecode.org/) 合作。

Aerotenna 团队使用了 DJI F550 机身，并计划很快在更多硬件上进行测试。他们的帖子中没有太多的技术细节，但是 Xilinx 的 Xcell 博客上的一篇帖子有更多的细节。在那篇文章中，[Aerotenna]的创始人之一说，Zynq 的 FPGA 部分允许他们更有效地进行实时处理，并处理计算密集型任务。提到了飞行动力学和多个视频馈送。

Zynq 板运行 Linux 和 ArduPilot 飞行控制软件(当然，这也是开源的)。Zynq 对于很多项目来说都是大材小用，但是驾驶一架大型无人机可能非常适合这么大的马力。最近我们已经看到了一些[整洁的 Zynq 板](http://hackaday.com/2015/10/07/arms-and-fpgas-make-for-interesting-dev-boards/)，包括对[的黑客攻击，将一个变成视差推进器](http://hackaday.com/2015/07/21/hackaday-prize-entry-an-fpgad-propeller/)，奇怪的是，这与飞行没有任何关系。

我们很惊讶[Aerotenna]没有发布他们飞行的任何视频。然而，您可能会对今年嵌入式 Linux 大会的主题演讲感兴趣，Dronecode 的[Andrew Tridgell]谈到了 Ardupilot 的架构。

 [https://www.youtube.com/embed/mFyeFDzbJR4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mFyeFDzbJR4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


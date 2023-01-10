# FPGA CNC

> 原文：<https://hackaday.com/2015/09/21/fpga-cnc/>

当您想到 CNC 控制器时，您可能会想到带有并行端口的 PC 或一些基于微控制器的解决方案，如 Smoothie Board。【Mhouse1】有不同的想法:[用 FPGAs 做 CNC 控制器](https://github.com/mhouse1/mechsoftronic)。

FPGA 本质上是并行处理的，因此处理 g 代码、计算曲线和加速度以及同时驱动多个步进电机对 FPGA 来说根本不是问题。大多数基于计算机的设计在试图同时驱动所有东西时会有轻微的延迟，这会引入一些机械抖动。更糟糕的抖动发生在当一些其他任务接管 CPU 时，你有一台旧 PC 试图运行一切。

平心而论，[mhouse 1]的设计确实在 FPGA 上包含了一个 Altera CPU 来处理 CPU 擅长的一些任务，但 FPGA 允许设计专门为手头的任务创建 I/O 设备。CPU 还运行一个 RTOS (MicroC OS II)和一个在控制 PC 上运行的 Python GUI。

如果你感兴趣的话，有一篇关于使用 FPGA 控制数控机床的旧文章，其中有很多关于设计这样一个庞然大物的有用信息。然而，那个设计远没有这个有野心。[Mhouse1]希望控制器是机器不可知的，他已经在一台廉价的基于 DVD 的激光切割机和一台经过修改的 Shapeoko 机器上演示了这一点。

如果你想了解 FPGA，你可能想从我们关于廉价 FPGA 开发的教程开始。或者，你可以用[的网络浏览器](http://hackaday.com/2015/07/21/learn-fpgas-in-your-browser/)学到很多东西。

 [https://www.youtube.com/embed/V51caXYTmaI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V51caXYTmaI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/i7nqlkxr84E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/i7nqlkxr84E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


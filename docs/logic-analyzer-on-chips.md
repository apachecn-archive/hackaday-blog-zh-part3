# 片上逻辑分析仪

> 原文：<https://hackaday.com/2017/05/17/logic-analyzer-on-chips/>

互联网上充斥着使用 CPU 的低速逻辑分析仪设计。基于 FPGA 的设计也不少。两者各有利弊。FPGAs 速度很快，可以同时处理大量数据。但是 CPU 通常有更多的内存，对主机进行 I/O 也更简单。[穆罕默德]回避了选择。他建造了一个逻辑分析仪，部分驻留在 FPGA 上，部分驻留在 ARM 处理器上。

事实上，他的理由是取代内置的 FPGA 逻辑分析仪，如 Chipscope 和 SignalTap。这些都是为了与你的 FPGA 设计共存，但[Mohammad]发现它们有局限性。它们还会占用你自己设计的空间，所以不可避免地，它们可能没有太多的内存。

该系统能够在 640×480 VGA 显示器上实时采集和显示 32 位信号。该系统还有一个 USB 鼠标接口，用于缩放和滚动显示。你可以在下面看到一段视频。

你可以选择仿真，但有时你真的需要在实际的芯片上运行你的设计。存在难以在模拟中建模的细微故障，甚至与其他硬件的交互。

该分析仪有几个有趣的设计特性，包括使用 Xillybus 内核来简化从 FPGA 逻辑到 ARM AXI 总线的接口。这大大简化了与 ARM 处理器的通信。

我们之前已经看过[基于 FPGA 的廉价逻辑分析仪](https://hackaday.com/2016/12/13/compiling-a-22-analyzer/)。如果您的设备上还有剩余空间，您可以使用这些集成设备。如果你觉得不需要速度，你可以选择基于 CPU 的[设计](https://hackaday.com/2015/12/04/a-teensy-logic-analyzer-for-a-6502/)。

 [https://www.youtube.com/embed/ouLi8tj1zsg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ouLi8tj1zsg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你不知道，这是布鲁斯·兰德学生的项目之一。感谢[Bruce]的提示和你为创造下一代硬件黑客所做的一切。
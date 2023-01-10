# Xilinx FPGAs 免费 C 语言版本

> 原文：<https://hackaday.com/2015/12/17/xilinx-fpgas-in-c-for-free/>

想到用 FPGAs 开发，通常会想到写 Verilog 或者 VHDL。然而，最近出现了一种趋势，即使用 C 来描述 FPGA 应该做什么，并有工具将其转换为 FPGA。然而，至少在 Xilinx 器件的情况下，这种能力只在他们的最新工具(Vivado)中可用，Vivado 并不针对大多数低成本开发板使用的较旧的低成本 FPGAs。

为 Xilinx 写博客的人有一个答案。原来你可以使用 Vivado C 编译工具为旧的 FPGAs 生成代码；只是涉及到不太方便的工作流程。Vivado(甚至是免费版本)生成独特的文件，工具的其余部分使用这些文件来获取编译后的 C 代码。然而，它也会生成 RTL (Verilog 或 VHDL)作为副产品，你可以把它导入到旧的 ISE 工具(它有一个非常好的免费版本)中，像对待任何其他 RTL 文件一样对待它。

下面的视频中有一个使用 Vivado 工具的例子。[Sleibso]指出，该视频已有三年历史，视频中关于许可的说法已经过时。免费工具现在包含了这个功能。[Sleibso]谈到使用 Spartan 6，但相同的分割工作流程应该适用于 ISE 支持的大多数设备。

值得注意的是，这并不等同于在 FPGA 上有一个 CPU 并用 C 语言编程(尽管 Vivaldo 也会这样做)。[Sleibso]提到的技术将 C 的子集转换成 FPGA 逻辑。如果你对在 FPGA 上使用 C 感兴趣，Xilinx 有[一个关于它如何工作的好文档](http://www.xilinx.com/support/documentation/sw_manuals/ug998-vivado-intro-fpga-design-hls.pdf)。如果您希望直接移植代码，请注意像动态内存分配这样的事情在 FPGA 上是不可能的。另一方面，在许多情况下，使用这种方法可以获得惊人的性能，特别是对于像视频处理或 DSP 这样的计算密集型软件。

如果你想从总体上了解更多关于 FPGA 的知识，以及与它们一起使用的传统 Verilog 语言，你可能会比[更糟糕。阅读我们的三部分教程，了解如何开始使用 iCEStick FPGA 板](http://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/)，或者阅读[更高级的教程，了解如何在目前正在开发的 FPGA 上实现 UART 控制的 PWM 控制器](http://wp.me/pk3lN-LgZ)。如果你喜欢 Python，也有一种方法[将其转换成 FPGA 配置](http://hackaday.com/2012/06/13/myhdl-python-programming-option-for-fpga/)。

 [https://www.youtube.com/embed/uXJ5rYhEfTE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uXJ5rYhEfTE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示。

斯巴达 6 号照片:大可(大可) [CC-BY-SA-3.0](http://creativecommons.org/licenses/by-sa/3.0/)) 通过维基共享
# 你要去 FPGA！

> 原文：<https://hackaday.com/2017/06/14/you-are-go-for-fpga/>

[Reconfigure.io](https://reconfigure.io/) 正在接受其环境的 beta 应用，以使用 Go 配置 FPGAs。是的，Go 是一种编程语言，但软件将代码转换成 FPGA 构造，所以你不需要 Verilog 或 VHDL。由于 Go 支持同步和通信的并发例程和通道，FPGA 的并行特性应该非常适合。

根据该项目的网站，该工具还允许您使用基于云的构建和部署系统来动态重新配置 FPGA。还没有太多的细节，除非你被接受为阿尔法。他们声称他们会优先考虑最有趣的用例，所以推销你闪烁的 LED 项目可能不会削减它。然而，在他们的 GitHub 网站上有更多的细节。

我们已经看到了用于 FPGAs 的 [C 编译器](https://hackaday.com/2017/04/26/fpgas-in-c-with-cynth/)(事实上，[不止一个](https://hackaday.com/2015/12/17/xilinx-fpgas-in-c-for-free/))。你也可以使用 [Python](https://hackaday.com/2012/06/13/myhdl-python-programming-option-for-fpga/) 。这有明显的不同吗？听起来可能是这样，但是在软件完全出现之前，现在下结论还为时过早。同时，如果你想要一个传统 FPGA 设计的速成班，你可以花大约 25 美元[买一些硬件](https://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/)，然后上路。
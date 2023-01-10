# Icestudio:一个开源的图形 FPGA 工具

> 原文：<https://hackaday.com/2016/02/23/icestudio-an-open-source-graphical-fgpa-tool/>

如果您曾经使用过 FPGAs，那么您已经处理过供应商提供的大量 ide。Xilinx 的 ISE 大约需要 6g，Altera 的 Quartus 超过 10g。光是让 LED 闪烁就要下载很多专有软件。

[Jesús Arroyo]的 [Icestudio](https://github.com/bqlabs/icestudio) 是一个新的图形化工具，可以让你从框图中生成 Verilog 代码，并在 Lattice Semi [iCEstick](http://www.latticesemi.com/icestick) 开发板上运行。拖放界面可以让你连接 IOs、逻辑门、分频器和其他元件。一旦你的框图准备好了，只需按一下按钮就可以将代码下载到冰棍上。

在引擎盖下，Icestudio 使用 [IceStorm](http://www.clifford.at/icestorm/) ，我们[已经在过去](http://hackaday.com/2015/05/29/an-open-source-toolchain-for-ice40-fpgas/)讨论过了，包括[这个由【Clifford】](http://hackaday.com/2015/12/29/32c3-a-free-and-open-source-verilog-to-bitstream-flow-for-ice40-fpgas/)主持的伟大演讲，IceStorm 的主角。对于 GUI，Icestudio 使用 [nw.js](https://github.com/nwjs/nw.js/) ，根据框图吐出 JSON。这个 JSON 被转换成 Verilog 文件和 PCF 文件。Verilog 用于创建 FPGA 上的逻辑，PCF 用于定义器件的引脚配置。如果你想知道实际发生了什么，点击选中的模块会显示生成的 Verilog。

这是实验性的，但这看起来是一种无需学习新语言或下载大量工具链就能开始使用 FPGAs 的好方法。我们希望 Icestudio 继续成长为教育和 FPGA 开发的有用工具。休息之后是演示。

【感谢[尼尔斯](http://www.silberkind.de/blog/)的提示！]

 【更新:新视频！]

 [https://www.youtube.com/embed/Okl4Rr_i6Qk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Okl4Rr_i6Qk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 树莓 Pi 的 FPGAs

> 原文：<https://hackaday.com/2015/10/18/fpgas-for-the-raspberry-pi/>

FPGA 开发在去年取得了巨大的进步，这完全归功于 Lattice 的 iCE40 FPGA 的开源工具链。去年春天，这种 FPGA 的比特流被逆向工程，工具链可用于任何可以运行 Linux 的设备，包括 Raspberry Pi。Xess [的[Dave]认为是时候推出 Raspberry Pi FPGA 板了](https://hackaday.io/project/7982-cat-board)。在这个开源工具链的帮助下，他可以在 Raspberry Pi 上对这个 FPGA 板进行编程。

[戴夫]的板子的灵感来自于 [XuLA](http://www.xess.com/shop/product/xula2-lx9/) 和 [StickIt！](http://www.xess.com/shop/product/stickit-mb-4_0/)给 Raspberry Pi 一顶 FPGA 帽子的电路板。这些电路板有一个问题:Xilinx 比特流必须在“真正的”PC 上编译，然后带到 Raspberry Pi 世界。新项目——CAT Board——为 Raspberry Pi 带来了完整的 FPGA 开发套件。

CAT 板的硬件是 Lattice iCE-HX8K、32m SDRAM、串行配置闪光灯、led、按钮、DIP 开关、grove 连接器和 SATA 连接器(尽管[Dave]只是将这些用于差分信号；他不知道他是否可以让 SATA 硬盘与此主板配合工作)。

尽管他的板房存在一些问题，但[Dave]最终让他的 FPGA 工作了，或者至少是比特流配置部分，他可以用树莓 Pi 和可编程逻辑来闪烁一对 led。这个项目的 Hello World 已经完成，现在唯一的限制是这个 FPGA 上有多少个门。

 [https://www.youtube.com/embed/RjpRsHvdC3k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RjpRsHvdC3k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


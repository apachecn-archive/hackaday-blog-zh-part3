# Linux 内核配置的 Lattice ICE40 FPGA

> 原文：<https://hackaday.com/2017/04/13/lattice-ice40-fpga-configured-by-linux-kernel/>

Linux 内核最近增加了通过 FPGA 管理器框架将固件加载到 FPGA 中的支持。[OpenTechLab]已经为 Lattice iCE40 FPGA 构建了[驱动程序(iCEStick 和其他开发板上使用的相同芯片)。iCE40 的一个吸引人之处是有一个叫做 iCEStorm 的开源工具链。](https://opentechlab.org.uk/videos:002:notes)

即使您对 FPGAs 不感兴趣，关于 Linux 设备驱动程序的讨论也是很好的背景。这些原则也适用于其他驱动程序，如果你想写另一个 FPGA 加载器，这些原则也绝对适用。

该示例使用连接到评估板的 Raspberry Pi。一个便宜的基于 Sigrok 的逻辑分析仪让他排除故障和调试。如果你觉得 FPGA 开发很贵，那就再想想。这里使用的主板不到 50 美元，软件是免费的。冰棍更便宜，可能在这里也管用。你可能有其他的东西，但是即使你需要买一个 Pi 和逻辑分析仪，整个东西也不到 100 美元。

我们在过去已经报道过[冰棍](https://hackaday.com/2015/08/27/learning-verilog-for-fpgas-hardware-at-last/)和[冰风暴](https://hackaday.com/2015/12/29/32c3-a-free-and-open-source-verilog-to-bitstream-flow-for-ice40-fpgas/)很多次了。也有相当多的 iCE40 板的树莓 Pi 应该可以很好地工作，包括[这个](https://hackaday.com/2017/02/08/adding-icezero-to-the-raspberry-pi/)。

 [https://www.youtube.com/embed/nIEB1VAGUcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nIEB1VAGUcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


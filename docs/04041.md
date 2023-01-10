# 给你的 RPi 一顶很酷的 FPGA 帽子

> 原文：<https://hackaday.com/2016/11/05/give-your-rpi-a-cool-fpga-hat/>

您的树莓 Pi 需要额外的自定义 IO 吗？添加 FPGA 是扩展 IO 的合理方式，并支持高速数字接口。[Eric Brombaugh]的 [Icehat](http://ebrombaugh.studionebula.com/embedded/icehat/index.html) 在一个封装中添加了一个点阵 [iCE5LP4K-SG48](http://www.latticesemi.com/en/Products/FPGAandCPLD/iCE40Ultra.aspx) FPGA，正好放在 Raspberry Pi Zero 的顶部。它还提供了一些 led 和 Digilent 兼容 PMOD 连接器，用于添加外设。FPGA 成本约为 6 美元，所以这是一块便宜的 FPGA 板。

FPGA 具有一次性可编程存储器，但也可以通过 SPI 编程。这允许主机 Pi 在引导时用最新的比特流来刷新 FGPA。遗憾的是，开源工具链不支持这个特殊的设备。相反，你需要 Lattice 的 [iCEcube2](http://www.latticesemi.com/iCEcube2) 设计软件。幸运的是，这个芯片是由免费许可证支持的。

Icehat 是一个开源硬件设计，但也包括一个软件应用程序，用于将比特流从 Pi 闪存到 FPGA，以及一个示例应用程序来帮助您入门。所有相关资料都可以在 [Github](https://github.com/emeb/icehat) 上找到，PCB 也可以在 [OSHPark](https://oshpark.com/shared_projects/arGUJG2i) 上找到。

虽然这不是我们看到的第一个 Raspberry Pi 和 FPGA 的组合，但它很可能是最小的，并且可以以低成本手工制作。
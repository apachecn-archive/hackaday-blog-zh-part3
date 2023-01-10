# 开源 FPGA Pi Hat

> 原文：<https://hackaday.com/2015/10/10/open-source-fpga-pi-hat/>

在 Hackaday.io 上，[Dave Vandenbout]已经发布了[CAT board](https://hackaday.io/project/7982-cat-board)，这是一个树莓派~~子板~~帽子，它具有一个点阵 FPGA，32mb RAM，EEPROM，以及一些 Grove 和 PMOD 连接器。CAT 利用了 Lattice 可用的开源工具链，包括基于 Python 的 MyHDL(不过，如果您愿意，也可以直接使用 Verilog)和 Icestorm。有趣的一点是:您可以在 Raspberry Pi 上运行工具链，从而形成一个自包含的、可移植的 FPGA 开发环境。

设计文件其实在 [Github](https://github.com/xesscorp/CAT-Board) 上。您可能会注意到 SATA 连接器。但是，[Dave]不知道您是否真的可以对它们使用 SATA 驱动器，它们是用于通用差分 I/O 的。

有一个用于 FPGA 开发的开源板和工具链是非常棒的。在和 [MyHDL](http://hackaday.com/2012/06/13/myhdl-python-programming-option-for-fpga/) 之前，我们已经讨论过[开源 Icestorm 工具链。如果您愿意，大多数供应商的 FPGA 工具都可以免费用于许多常见设备和用途。Lattice 工具应该可以很好地与这个板一起工作，即使它确实冒犯了您的开源敏感性。](http://hackaday.com/2015/08/27/learning-verilog-for-fpgas-hardware-at-last/)

下面的视频介绍了猫的董事会，但被警告:它确实包含实际的猫图片。然而，它不包含对苏斯博士的任何道歉。

 [https://www.youtube.com/embed/EHtcOrdl9Xw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EHtcOrdl9Xw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


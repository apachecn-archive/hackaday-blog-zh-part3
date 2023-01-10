# 将 IceZero 添加到树莓酱中

> 原文：<https://hackaday.com/2017/02/08/adding-icezero-to-the-raspberry-pi/>

[Kevinhub]注意到树莓 Pi 有相当多的 FPGA 帽子。他没有像一个肮脏的平民一样出去买一块这样的板，而是决定组装自己的 FPGA Pi 配件。这款 IceZero FPGA 板结合了其它 FPiGA 板的最佳特性，其外形正好适合极小的 Pi Zero。

如果你认为把一个点阵式 FPGA 放在一个 Pi 上已经有人做过了，那你就对了。这里有一顶使用 [iCE5LP4K-SG48](http://www.latticesemi.com/en/Products/FPGAandCPLD/iCE40Ultra.aspx) 的 Pi 的帽子，这是一个具有 3520 个 lut 的 FPGA。[Xess](http://hackaday.com/2015/10/18/fpgas-for-the-raspberry-pi/)的 CAT 板有一个稍大的 FPGA，有 7680 个逻辑单元，[的 FleaOhm](http://hackaday.com/2016/10/02/hackaday-prize-entry-fpgas-for-the-raspberry-pi-zero/) 板上有一个巨型 FPGA，价格约为 70 美元。

【Kevin】的 IceZero 在这些树莓 Pi FPGA 帽子的下端，用的是格子 ICE40HX4K。只有 3520 个逻辑单元，但第一批只需 7 美元。电路板设计是一个标准的两层电路板，对于手工焊接来说不会太糟糕。如果你想测试这个小家伙的话，这些板子在奥什公园上是共享的。

这款 Pi Hat 专门设计用于 Project IceStorm，这是 Lattice 的 iCE40 FPGAs 的开放工具链。这意味着已经有一些项目可以很容易地移植到这个平台上，而且[Kevin]已经有了一个逻辑池示例放在他的板上。
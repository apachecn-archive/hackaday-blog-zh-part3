# Hackaday 奖参赛作品:树莓派中的真正硬盘

> 原文：<https://hackaday.com/2017/04/12/hackaday-prize-entry-real-hard-drives-in-the-raspberry-pi/>

伙计，我希望树莓酱有一个 SATA 端口。这是在互联网上回响的请求，这一次，互联网没有错。SATA 端口——或者任何连接到一个大而笨的旋转磁盘的连接器——将会是 Raspberry Pi 生态系统的一大亮点。

[AlanH]进入 Hackaday 奖[与每个人想要的](https://hackaday.io/project/20774-netpi-ide)完全相反。NetPi-IDE 是一个并行 ATA IDE 磁盘模拟器，它可以将一个便宜的 Raspi Zero 变成一个又大又笨的非旋转硬盘。将这台机器放入你的 Windows 98 星际争霸战斗站，你就有了一个可以 ssh 的硬盘。

与任何涉及大量数据的构建一样，带宽非常重要。Pi 的 GPIO 端口上带宽最高的接口是 SPI 接口。[AlanH]正在将 Lattice MachXO2 FPGA 挂在 SPI 端口上，并使用它来模拟磁盘。在未来，他将转向更加开放的晶格 iCE40HX，与开源 IceStorm 合成链兼容。

这个项目的特性集包括合适的 IDE 磁盘模拟，到目前为止测试的大小从 10mb 到 8gb 不等。如果你需要更大的东西，你不需要 IDE 驱动器。DOS 重定向器允许将任意目录挂载到 DOS 驱动器盘符，虚拟网络接口将该项目转化为 Cloud，串行控制台映射到未使用的 IDE 寄存器，允许任何主机系统无需任何外部电缆即可登录到 Pi。

虽然这不是每个人都想要的 Pi，但这是一个非常酷的项目。PATA 硬盘越来越旧，支持它们的系统也越来越旧。如果你想让这些逆向计算机继续运行，我们必须现在就开始计划，没有比廉价的硬件和开源工具链更好的方法了。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
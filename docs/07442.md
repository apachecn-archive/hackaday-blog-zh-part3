# Hackaday 奖参赛作品:用自己编程 FPGAs

> 原文：<https://hackaday.com/2017/10/23/hackaday-prize-entry-programming-fpgas-with-themselves/>

自第一个面向 FPGAs 的开源工具链推出以来，已经过去了几年。你可能会认为一种免费和开放的 FPGA 编程方式将有利于硬件开发，但迄今为止，我们真的没有看到一种小型、廉价、智能的设备将 FPGA 带到大众面前。

我们不知道[【Luke】进入 Hackaday 奖](https://hackaday.io/project/26848-tinyfpga-b-series)是否是将做到这一点的杀手级项目，但它非常简洁。他使用 Lattice iCE40 FPGA 设计了一个微型 FPGA 开发板，能够通过 USB 进行自我编程。它很小，很便宜，很容易使用，并且有使用该板进行 FPGA 开发的工作实例。

如果你觉得这个小小的板子看起来很眼熟，那你就对了。[Luke]一直在开发类似的主板，[A 系列](https://hackaday.com/2017/07/31/tinyfpga-is-a-tiny-fpga-board/)，但这个最新版本有一个 USB 端口，而不是 JTAG 适配器的引脚。这种 USB 功能非常聪明——Luke 没有使用单独的微控制器，而是使用 FPGA 本身将用户配置重新编程到闪存芯片中。一旦启动并运行，引导加载程序将被删除，并且不会消耗任何 FPGA 资源。

[Luke]还在编写一份令人惊叹的 FPGA 爱好者指南,该指南非常依赖这些点阵 FPGA 和他的开发板可用的开源工具链。这对社区来说是一个巨大的好处，也是获得 Hackaday 奖的绝佳机会。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
# Zedboard 多端口以太网

> 原文：<https://hackaday.com/2016/01/08/zedboard-multiport-ethernet/>

Zedboard 用的是 Xilinx 的 Zynq，是 ARM CPU 和 FPGA 的组合。[Jeff Johnson]最近发布了一篇精彩的[两部分教程，讲述了如何使用带有多个以太网端口的 zed board](http://www.fpgadeveloper.com/2015/12/using-axi-ethernet-subsystem-and-gmii-to-rgmii-in-a-multi-port-ethernet-design.html)。lwIP(轻量级互联网协议)栈负责软件端。

Vivado 是 Xilinx 用于配置 Zynq(以及其他芯片)的软件，本教程将向您展示如何使用它。以太网 PHY 是一种商用的带四个端口的 FPGA 夹层卡(FMC)。项目使用 VHDL，但不涉及 VHDL 编码，只是使用封装组件。

使用 FPGA 和 CPU 时，真正的问题是处理器和 FPGA 电路之间的接口。在这种情况下，ARM 标准 AXI 总线执行此任务，以太网组件与该总线正确接口。帖子第二部分的 IP 应用[是一个 echo 服务器。](http://www.fpgadeveloper.com/2016/01/running-a-lwip-echo-server-on-a-multi-port-ethernet-design.html)

我们已经看到 Zynq 在飞行器和音乐合成器中的应用。虽然这个项目没有使用您创建的任何 Verilog 或 VHDL，但它仍然是使用 Vivado 配置和在设计中使用通用组件的一个很好的例子。
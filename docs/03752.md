# 开放式设计示波器可以(几乎)免费

> 原文：<https://hackaday.com/2016/10/06/open-design-oscilloscope-could-be-almost-free/>

如果你只能拥有一台测试设备，它应该是一台示波器。话又说回来，现代示波器通常有多种功能，所以这可能不是一个公平的断言。一个恰当的例子是 [Scopefun 开放硬件项目](http://www.scopefun.com/)。该设备是一个功能强大的双通道示波器、逻辑分析仪以及波形和模式发生器。控制 GUI 可以在 Windows、Linux 或 Mac 上运行(见下面的视频)。

硬件使用 Xilinx Spartan-6 FPGA。GUI 使用 Cypress 的 EZ-USB FX2LP 芯片向 FPGA 发送配置数据。两个示波器通道都受到最高+/- 50 V 过压保护，FPGA 通过一个 10 位双通道模数转换器(ADC)以 100 Mhz 进行采样。FPGA 处理触发并缓冲输入，然后通过 USB 芯片将数据发送到主机。每个通道都有一个 10，000 个样本的缓冲器。

还有两个带短路和过压保护(+/- 50 V)的发电机输出。发生器通道具有 50 欧姆的内部阻抗，也可使用相同的 USB 芯片通过 GUI 进行操作。FPGA 利用计数器、算法或简单波形数据产生 50 Mhz 信号，并馈入 DAC。

16 位数字接口可以设置为输入或输出。FPGA 以 100 MHz 的速率对输入进行采样。输出电压可以设置，但输入可以接受 5 V 电压。

根据开发商的说法，您可以通过使用来自各个供应商的免费样品芯片从提供的信息中构建范围，只需支付小组件和 PCB 的成本。

我们之前已经看过几个低成本范围选项。 [Labtool](https://hackaday.com/2016/01/27/a-tale-of-two-sub-100-oscilloscopes/) 甚至拥有一些类似的功能。

 [https://www.youtube.com/embed/mdjJTs8R46g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mdjJTs8R46g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


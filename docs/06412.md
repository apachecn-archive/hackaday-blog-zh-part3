# 试验板 RF103

> 原文：<https://hackaday.com/2017/07/01/the-breadboard-rf103/>

当[ik1xpv]着手打造软件定义无线电(SDR)的时候，他并没有胡来。他的[试验板 RF103](http://www.steila.com/blog/index.php?controller=post&action=view&id_post=18) 支持 USB 3.0 和 16 位模数转换器，采样速率最高可达 105 Msps，接收频率范围为 0 至 1800 MHz。还不错。得益于 USB 3.0 端口，所有信号处理都在 PC 中进行，而没有通过通用声音端口传输数据的限制。你可以在下面的视频中看到这个设备的运行。

Cypress FX3 USB 设备是 ARM 处理器，但它只是流数据，而不是处理数据。你可以在 [GitHub](https://github.com/ik1xpv/BBRF103) 上找到稍加修改的固件、使用 PC 软件的驱动程序、原理图和电路板布局。

我们不太确定术语“试验板”在名称中的位置，因为涉及到 PC 板，没有无焊试验板。基本接收机覆盖 0 至 30 MHz，混频器将较高频率下变频至该范围。

有足够的信息，你应该能够复制这个项目，尽管你需要做一些材料的分析。这不是一步一步的构建教程。然而，这应该比常见的 [RTL-SDR 加密狗](https://hackaday.com/2017/01/27/raspberry-pi-sdr/)复杂得多。这与 [SDRPlay](https://hackaday.com/2015/11/12/your-first-gnu-radio-receiver-with-sdrplay/) 更接近，尽管它有更高的最大频率和一些额外的硬件滤波。它也是一个 12 位数字化仪，而不是 RF103 的 16 位数字化仪，这是 RF103 的优势之一。

 [https://www.youtube.com/embed/V4i-ekfWK-k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V4i-ekfWK-k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


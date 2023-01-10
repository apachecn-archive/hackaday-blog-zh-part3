# USB 转四路串行端口适配器提供 TTL 隔离端口

> 原文：<https://hackaday.com/2018/02/10/usb-to-quad-serial-port-adapter-offers-ttl-isolated-ports/>

[Felipe Navarro]想给他的计算机添加几个串行端口，但找不到适合他需求的适配器。所以，他自己造了一个。

他的[四串行设备](https://github.com/PY1CX/Quad-Serial)是一个设计精美的转换器，提供四个串行端口，其中两个是隔离的，以避免出现问题时引爆太多东西。另外两个是 TTL 端口，但有一个有趣的变化:给它们提供 1.8 V 到 5 V 之间的任何电压，它们都会很高兴地工作，这比摆弄 TTL 到 RS-232 转换器要容易得多。

它完全是围绕 FTDI FT4232H 芯片构建的，该芯片有适用于大多数操作系统的驱动程序，因此它应该可以与几乎任何东西一起工作。而且，正如[Felipe]指出的，这种芯片没有被克隆，所以你不必担心 FTDI 驱动程序会在没有警告的情况下禁用你的设备。嗯，反正现在没有。我们去年确实报道过一个类似的[四串口适配器](https://hackaday.com/2016/07/22/quad-serial-adapter/)，但是这个更先进一点，有 DE-9 和螺丝终端连接器。
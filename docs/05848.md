# 全栈 GPS 接收机

> 原文：<https://hackaday.com/2017/05/09/a-full-stack-gps-receiver/>

将 GPS 功能添加到项目中的通常方式是抓取现成的 GPS 模块，将其插入 UART，并从串行端口读取 NMEA 句子流。取决于你在 GPS 模块上花了多少钱，这很好:那里最好的模块启动很快，而且他们中的许多人都认识到 ITAR 规则中的逻辑和。

对于[Mike]来说，获取现成的模块是不可能的。他正在使用一点硬件和 FPGA 技术从头开始建造自己的 GPS 接收器。他已经取得了很好的结果，他不必再去理会那些乱七八糟的“不要建造弹道导弹”的法律。

这个构建的硬件包括一个用于 BeagleBone 的[Kiwi SDR“cape”](http://kiwisdr.com/)和一个 Digilent Nexus-2 FPGA 板。SDR 板采集 16.268 MHz 的原始 1 位样本，需要采集一整分钟的数据。FPGA 至少要整理 120 兆字节的数据。

这个项目的软件首先通过找到近似的频率和相位来获取 GPS 信号。然后，软件锁定载波，计算出相位，并接收 50bps 的“导航”信息，这是找到天线位置的定位解决方案所必需的。这个软件的第一个版本非常慢，需要 6 个多小时来处理 200 秒的数据。现在，[Mike]改进了通道跟踪代码，速度提高了 300 倍。那就是使用商品现成的硬件实时处理 GPS 数据。所有的软件[都可以在 Gits](https://github.com/hamsternz/Full_Stack_GPS_Receiver) 上获得，这使得这个项目很容易被任何人复制。我们预计美国国务院或国防部会很快拜访[迈克]。

当然，这不是第一次有人从零开始制造 GPS 接收器。几年前，[利用 FPGA 和自制 RF 板，可以实现小于 1 米的精度](http://hackaday.com/2013/05/17/homebrew-gps-gets-%C2%B11-meter-resolution-with-a-raspberry-pi/)。
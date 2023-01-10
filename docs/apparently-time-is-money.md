# 显然时间就是金钱

> 原文：<https://hackaday.com/2017/04/13/apparently-time-is-money/>

有些人喜欢改装汽车。有些人喜欢电脑超频。还有像杰克·齐默曼这样痴迷于精确时间的人。他正在进行一个项目，该项目将在不同的非洲国家部署 NTP(网络时间协议)服务器，并且需要小型、廉价、节能和精确的服务器。他最终得到的是[一个非常精确的设置](http://www.jackenhack.com/ntp-server-extreme-accuracy-for-under-200/)大约 200 美元。在此过程中，他构建了一些定制硬件，并入侵了一台计算机来同步 GPS 时钟参考。

他最初的尝试是用覆盆子 Pi 3。然而，网络适配器不是最快的，因为它是 100 MBPS，主要是因为它是通过 USB 总线连接的。由于这些限制造成的网络延迟使得提供准确的时间变得困难。

他的解决方案包括一个 Odroid C2。售价 50 美元，这是一台非常强大的四核计算机，千兆以太网，甚至可以使用比普通 SD 卡更快的 eMMC 存储。不过，如果你愿意，你仍然可以使用传统的 SD 卡。

[Jack]使用 Trimble GPSDO (GPS 规定的振荡器)作为时间基准，输出一个 PPS(每秒脉冲数)和两个 10 MHz 信号。这些被锁定在 GPS 卫星时钟上，这些时钟非常精确，[杰克]说时间精确到不到 50 纳秒。不幸的是，Trimble 板的脉冲太短，无法读取，所以他设计了一个脉冲拉伸电路。

[Jack]没有尝试将 Odroid 上现有的时钟调整到 GPS 基准，而是完全移除了水晶和相关组件。然后，他使用频率发生器芯片将 10 MHz GPS 信号转换为 Odroid 期望的 24 MHz 时钟。他还计划使用芯片的额外输出来驱动以太网和 USB 时钟，尽管它们的绝对精度可能不是那么关键。

我们以前见过 NTP 时钟会消耗这种时间参考。如果你想[了解更多关于](https://hackaday.com/2016/03/16/hands-on-with-the-odroid-c2-the-raspberry-pi-3-challenger/) Odroid [C2](https://hackaday.com/2016/03/16/hands-on-with-the-odroid-c2-the-raspberry-pi-3-challenger/) 的信息，我们去年已经详细讨论过了。
# 提高 Raspberry Pi 磁盘性能

> 原文：<https://hackaday.com/2016/12/29/improving-raspberry-pi-disk-performance/>

通常，你会认为固态存储比旋转硬盘更快。然而，在 Raspberry Pi 的情况下，固态“磁盘驱动器”是一个使用串行接口的存储卡。因此，虽然 7200 RPM SATA 驱动器可能获得超过 100MB/s 的速度，但 Pi 的性能明显较低。

[Rusher]在他的 Raspberry Pi 上使用 Gluster 分布式文件系统和 Docker。他测得的写入性能为缓慢的 1MB/s(根文件系统的时钟速度刚刚超过 40MB/s)。

有无数的设置可以调整，但[拉什尔]试探性地选择了几个他认为会有影响的。经过一些试验后，[他在 Gluster 上管理 5MB/s，并将普通文件系统增加到 46 MB/s](https://www.linux-toys.com/?p=1153) 。

我们可能已经研究了与存储卡的实际缓冲和读取以及 I/O 调度更相关的几个其他设置。然而，[Rusher]向您展示了他的方法，所以如果您想以此作为进一步探索的起点，或者您想使用不同的文件系统，它仍然值得一看。

我们倾向于认为 Pi 是一个嵌入式板。但实际上，它只是另一个 Linux 平台，并且已经针对不同的情况做了很多优化 Linux 性能的工作。我们之前也研究过[基于 Docker 的集群](http://hackaday.com/2016/08/29/raspberry-pi-hive-mind/)。
# 重新利用动圈式电表来监控服务器性能

> 原文：<https://hackaday.com/2017/08/31/repurposing-moving-coil-meters-to-monitor-server-performance/>

时髦的模拟仪表几乎可以为任何项目带来复古风格，但最近它们似乎经常被重新分配为指示器，用于与最初预期完全不同的用途。对于[来说是这样的，这些 Vu 计量器被重新用作 Raspberry Pi 服务器](https://hackaday.io/project/26951-audio-vu-meters-raspberry-pi)的计量器，我们认为构建日志的信息量与成品的外观一样大。

正如[MrWunderbar]所承认的那样，动圈式电表的跳舞针为一个项目增添了潮人的可信度，但让他的 Vu 电表协同工作，并在他的 Raspberry Pi NAS 服务器上显示网络利用率和磁盘 I/O，可不是一件容易的事。他的构建日志中有很多关于如何测量电表内阻和确定合适串联电阻的详细信息。他还长篇大论地讨论了使用 PWM 信号或 DAC 驱动电表的相对优势；最终，[MrWunderbar]选择了 DAC 路线，下面的视频显示了随着磁盘和网络使用情况的变化，所需的快速而平稳的摆动。他还深入研究了从 psutil 中提取使用参数并解析结果以显示在血糖仪上。

寻找更多模拟仪表优点？几个月前，我们看到了类似的 CPU 负载测量仪(T1 ),还有太阳能首席执行官办公桌上的(T2)混合了 Nixies 和旧测量仪(T3)。

[https://videopress.com/embed/VtHbcHKq?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0](https://videopress.com/embed/VtHbcHKq?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0)
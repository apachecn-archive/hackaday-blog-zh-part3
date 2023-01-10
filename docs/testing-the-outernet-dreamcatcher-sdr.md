# 测试 Outernet Dreamcatcher SDR

> 原文：<https://hackaday.com/2017/06/20/testing-the-outernet-dreamcatcher-sdr/>

当你把基于 ARM 的 Linux PC 和 RTL-SDR 交叉使用时，你会得到什么？听起来像是一个笑话的开头，但答案是 Outernet 的捕梦网。它是一个单 PCB，内置 RTL-SDR 软件定义无线电、L 波段 LNA 和 Allwinner A13 处理器，具有 512 MB RAM 和 1 GHz 时钟速度。rtl-sdr 网站最近发布了一篇对 99 美元主板的好评。

我们会让你自己阅读评论，但结论是，尽管有一些错误，主板并不比单独将零件组装在一起更昂贵。另一方面，如果你使用，比如说，Raspberry Pi 3，你可能会期望更多的支持和更高的性能。

尽管有 L 波段硬件，但有一个旁路天线插孔，允许您接收其他频率。还有两个 SD 插槽，一个用于启动，另一个用于存储。几个软件在有点慢的 CPU 上运行有问题，尽管一些软件针对所用的特定处理器进行了优化，运行得更好。你可以在评论里读到细节。

该板很有趣，尽管除非你有特殊的封装问题，否则你可能最好结合一个 Pi 和一个加密狗，就像我们在之前多次看到的[。如果你有更多的马力，你甚至可以使](https://hackaday.com/2016/12/05/an-amateur-radio-repeater-using-an-rtl-sdr-and-a-raspberry-pi/) [Pi 传输](https://hackaday.com/2013/11/09/transmitting-data-with-a-pi-and-rtl-sdr/)，虽然我们建议一些过滤，如果你真的要这样做。
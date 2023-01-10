# 超频的树莓 Pi 3 美味的速度提高

> 原文：<https://hackaday.com/2016/03/03/overclocking-the-raspberry-pi-3-for-tasty-speed-increases/>

有些人永远不会快乐。[Jackenhack]得到了几个闪亮的新的 Raspberry Pi 3s，他做的第一件事就是开始超频。幸运的是，他知道他在做什么，所以没有一个魔术烟逃脱，但似乎不是所有的 pi 都满意这个过程。

对于三个看似相同的 Pi 3 中的一个，添加散热器让他可以将 CPU 从原生的 1.2GHz 提升到 1.45GHz。这确实涉及到一点过压(增加 CPU 的电压)，但这可以很容易地在软件中完成。他还尝试给内存添加散热器，然后提高内存速度以增加吞吐量。同样，他能够取得一些令人印象深刻的进展，将速度从原来的 400 Mhz 提高到 500 Mhz。这两个都是稳定的超频:他能够在 100%的 CPU 负载下长时间运行系统，并将超频的 Pi 集成到他的系统中，为 [NTP 池项目](http://www.pool.ntp.org/en/)做出了贡献。

然而，当他用第二个 Pi 3 ~~受害者~~测试对象尝试相同的超频时，由于 CPU 过热而失败。因此，在 Pi 3 上，硅的各个位似乎有很多变化。也许一些液氮会有帮助？对于[一个 Arduino…](http://hackaday.com/2013/08/18/liquid-nitrogen-finally-makes-an-arduino-project-cool/)
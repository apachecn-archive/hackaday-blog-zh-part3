# 6502 的小型逻辑分析仪

> 原文：<https://hackaday.com/2015/12/04/a-teensy-logic-analyzer-for-a-6502/>

[John]在他的工作台上放着一个有趣的旧技术。这是俄亥俄州的科学 C3-8P 计算机从 70 年代后期通过一些车库，地下室和阁楼。与这个时代的大多数技术一样，存在一些问题，而且[John]发现没有跟踪和观察程序的能力，调试有点令人沮丧。他需要一个逻辑分析仪，并在一个不太可能的硬件中找到了一个。[John] [使用一个 Teensy 微控制器](http://lockett.altervista.org/logic65/logic65.html)建造了一个，这个项目的进一步完善可以将它变成一个完整的系统内仿真器。

[约翰]试图起死回生的老俄亥俄州科学计算机是基于 6502 CPU 的。这需要监控 16 条地址线、8 条数据线和 4 条控制线。这些是直接连接到一个小小的 3.1 上的。

读取和控制来自 6502 的所有信号是 Linux 的任务。命令行程序控制 Teensy，能够读取内存、设置触发地址、将整个地址空间转储到一个文件中，或者只记录最近的 5000 个时钟周期。这种技术早在 70 年代末和 80 年代初就存在了。也花了一大笔钱。现在，只要 20 美元的小玩意，再加上大概 30 美元的带状电缆和测试夹，任何人都可以为一个非常古老的计算机系统建造一个逻辑分析仪。

下面的视频。

 [https://www.youtube.com/embed/MZiIxxXJEkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MZiIxxXJEkE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/OakOfABBgsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OakOfABBgsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 解码从阿波罗导航计算机重新发现的绳索记忆

> 原文：<https://hackaday.com/2016/09/02/decoding-rediscovered-rope-memory-from-the-apollo-guidance-computer/>

1966 年 8 月 25 日，阿波罗指令舱在 AS-202 任务中由土星 IB 火箭发射升空。这项任务旨在紧接命运多舛的阿波罗 1 号任务之前，AS-202 是无人驾驶的，作为飞行硬件、燃料电池、制导和导航控制系统的测试。这项任务使用了第一台阿波罗导航计算机，这项任务对于测试将人类送上月球的计算机至关重要。

虽然后来的任务中的软件仍然存在，并可在 Github 上获得，但早期的 Block I 航天器，包括无人驾驶的阿波罗 4 号和阿波罗 6 号任务，都没有得到很好的记录。[Francois Rautenbach]很幸运地从 AS-202 任务中拿到了绳索记忆模块。[现在，他正在用示波器和 x 射线研究这些模块](https://www.youtube.com/watch?v=WquhaobDqLU)，以重现第一批在太空中飞行的软件。

从这些 rope 内存模块中提取数据的过程比从芯片上读取一点闪存要困难一些。绳索存储器很奇怪，但是通过一个由许多继电器和示波器组成的装置，[Francois]能够从这些存储模块中捕获数据。

当然，[Francois]首先需要找出每个内存模块上巨大背板连接器的引脚排列。为了做到这一点，[他检查了一个 Block II AGC](https://www.youtube.com/watch?list=PLw9205HNg8FFJxxgbVTxo5Z60BmlbMM1P&v=OkFy30kxfh4) ，非常仔细地阅读了原理图，并对一个不再生产的连接器进行了逆向工程。下一步是[对 rope 内存模块](https://www.youtube.com/watch?v=-BlivdwXRZU)进行 x 光检查，看看它们是如何组装的。即使这些内存模块包含 Block I AGC 软件的唯一现存副本，即使读取这些模块中的一位也是技术考古的一个惊人案例。

这个显而易见的问题的答案——这些模块从何而来——正是您所期望的。这些内存模块是 40 年前从废品堆里捡出来的。发现这些模块的先生好心地把它们给了[弗朗索瓦]。查看下面的视频，了解[Francois]的视频日志。如果你对被遗忘的阿波罗飞行硬件的破坏性测试稍感兴趣，几年前，[弗兰布兰奇]从阿波罗[运载火箭数字计算机](http://hackaday.com/2013/11/01/deconstructing-apollo-flight-hardware/)上拆下了几个模块。

感谢[Vincent]、[Danie]和[Kent]抓住这个机会，将它发送到举报热线。

 [https://www.youtube.com/embed/WquhaobDqLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WquhaobDqLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/-BlivdwXRZU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-BlivdwXRZU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


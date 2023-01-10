# 测试 DRAM，一次一个字节

> 原文：<https://hackaday.com/2016/03/18/testing-dram-one-byte-at-a-time/>

几个周末前，[克里斯]想玩一些复古游戏。这意味着要挖出配有巨大 RAM 卡的旧 Apple IIgs，它有整整三兆的 RAM。这个特殊的苹果 IIgs 有很长一段时间断断续续的问题，[克里斯]开始怀疑内存是罪魁祸首。测试这一点需要测试几十个独立的 RAM 芯片，所以[为什么不用 Arduino](http://www.insentricity.com/a.cl/252/testing-dram-using-an-arduino) 构建一些东西来让[Chris]的生活更轻松呢？

[克里斯]苹果公司的芯片是标准的 1m×1 DRAM 芯片，这是 80 年代后期电脑的标准。为了在 Arduino 上测试这些芯片，他拿起一个漂亮的 ZIF 插座，将芯片连接到 Arduino 防护罩上，开始了解决如何将 DRAM 连接到 Arduino 的快乐过程。

与静态存储器不同，DRAM 需要定期刷新以给电容器充电。虽然这种刷新周期一直是设计师和工程师的祸根，但[Chris]实际上并不需要关心 DRAM 的刷新。他只是将 1024 行写入内存，然后直接读取出来——不需要刷新内存。窍门来自多路复用地址总线。在他的项目中，[Chris]需要写入 10 位地址，锁存它，然后写入另一半地址位。

DRAM 测试很成功，[克里斯]把所有的代码和原理图[放到了 GitHub](https://github.com/FozzTexx/DRAM-Tester)上。解开苹果 IIgs 损坏之谜并不简单，因为[Chris]认为问题可能出在巨大的 RAM 卡或 IIgs 主板上的一个支持芯片上。尽管如此，这是一个整洁，快速的构建来测试几个 DRAM 芯片。
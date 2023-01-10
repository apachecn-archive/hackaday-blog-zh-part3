# 将反向散射无线电用于土壤传感器网络

> 原文：<https://hackaday.com/2017/03/03/using-backscatter-radio-for-a-soil-sensor-network/>

有近 80 亿人要养活，气候变化要应对，这是一个建设有意义的“农业互联网”的最佳时机。但是，使工业规模农业可行的广阔领域不利于传感器和致动器的部署，因为缺乏供电和连接一切的基础设施。因此，用于土壤湿度传感器的低功率无线电网络肯定是一个受欢迎的发展。

我们可以想出很多在现场给传感器供电的方法。我想到了太阳能，因为良好的阳光照射通常是任何农田的先决条件。但在实践中，太阳能有问题，主要是植物更需要阳光，并且会很快遮蔽低姿态的土壤传感器。

这就是为什么[Spyros Daskalakis]在他的电容式土壤湿度传感器中避免使用光伏电池，而是采用一种反向散射技术，这种技术非常类似于在[大海豹虫](http://hackaday.com/2015/12/08/theremins-bug/)和普通 RFID 标签中使用的技术。土壤传感器以与土壤湿度成比例的频率将蚀刻的 PCB 蝶形天线的一半接入和断开电路。来自独立发射机的载波信号被交替加载和卸载的天线反射，拾取频率与土壤湿度成比例的副载波。[Spyros]在[的论文](http://daskalakispiros.com/files/daskalakis_mtt_2015.pdf)中解释了更多关于传感器设计和他处理多个传感器的技术。

我们真的很喜欢这里运用的原则和系统的简单性。我们不禁想知道这个项目和 2015 年 Hackaday 获奖的 Vinduino 项目之间有什么样的协同效应。

 [https://www.youtube.com/embed/_kkxNAqPGqY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_kkxNAqPGqY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via[RTL-SDR.com](http://www.rtl-sdr.com/rtl-sdr-based-wireless-backscatter-soil-moisture-sensor-network/)
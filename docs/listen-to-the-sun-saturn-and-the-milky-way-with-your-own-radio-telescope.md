# 用你自己的射电望远镜聆听太阳、土星和银河系

> 原文：<https://hackaday.com/2016/09/28/listen-to-the-sun-saturn-and-the-milky-way-with-your-own-radio-telescope/>

来自印度科学教育和研究所的学生将一个商业卫星天线、一个卫星探测器和一个 Arduino 组合在一起，制作了一个可工作的射电望远镜。圆盘式卫星电视天线提供 LNB(低噪声模块),相关的机顶盒仅用于供电。他们的 LNB 采用铝箔屏蔽来阻挡外来信号。

除了硬件，该团队还构建了 Python 软件来分析数据，并展示了几个实际应用。他们使用已知的地球同步卫星来校准来自探测器的信号(由 Arduino 数字化)，以确定每单位电压的功率。他们还计算了光束宽度(约 3.4 度)，并使用太阳进行其他校准步骤。

该论文指出，一些设计使用普遍存在的 RTL-SDR，但这将带宽限制在 3 MHz 左右。卫星探测器本身是宽带的，该团队声称其范围的带宽为 1.1 GHz。一些设计(如 [Itty Bitty](https://hackaday.com/2016/07/31/the-tiny-radio-telescope/) )使用双通道 LNB 来实现这两者。如果你懒得建造任何硬件，你仍然可以进入[射电望远镜数据处理游戏](https://hackaday.com/2016/08/30/citizen-scientist-radio-astronomy-and-more-no-hardware-required/)。

如果你想了解射电天文学，你可能会喜欢约翰·摩根博士的讲座，在下面的视频中。

 [https://www.youtube.com/embed/_2EBCzyrqTA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_2EBCzyrqTA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


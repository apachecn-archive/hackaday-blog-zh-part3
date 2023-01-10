# SDR IF 实验

> 原文：<https://hackaday.com/2018/04/18/sdr-if-experiments/>

R820T 调谐器 IC 用于流行的 Airspy 软件定义无线电(SDR)以及许多廉价的 RTL SDR 加密狗。[TLeconte]对芯片的中频(IF)配置做了一些实验，你会[发现他的结果很有趣](https://tleconte.github.io/R820T/r820IF.html)。

使用每秒 500 万个样本和设备的真实模式，测试查看当 IC 读取噪声源时会出现什么。有两个寄存器设置 IF 参数，但测试显示了这些寄存器的精确效果。

根据帖子，有三件事可以设置:

*   粗中频滤波器带宽:窄/中/大
*   手动微调 IF 滤波器带宽，从 0(大)到 15(窄)
*   高通滤波器频率从 0(高)到 15(低)

由于混叠，有些设置没有意义，至少在 5 MHz 采样速率下没有意义。但是，看看每个设置的作用是很有启发性的。[TLeconte]使用[倍频程](https://hackaday.com/2016/06/30/tutorial-on-signal-processing-in-linux-with-octave/)来可视化数据。

如果您想从总体上了解更多关于 SDR 的信息，我们有[一些东西可以帮助您入门](https://hackaday.com/2016/05/30/hackaday-dictionary-software-defined-radio-sdr/)。如果你想自己做测试，可以考虑使用 [GNU Radio](https://hackaday.com/2015/11/11/getting-started-with-gnu-radio/) 。
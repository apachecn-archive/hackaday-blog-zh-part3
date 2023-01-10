# 用这个简单的微控制器 CPU 仪表了解负载

> 原文：<https://hackaday.com/2017/08/05/know-the-load-with-this-simple-microcontroller-cpu-meter/>

你怎么知道一个 CPU 上有多少负载？在台式机或笔记本电脑上，操作系统通常有某种小工具来显示基本信息。然而，在微控制器上，你必须[用几个部件、一些代码和一个电压表来组装你自己的 CPU 负载表](http://shadetail.com/blog/ghetto-cpu-busy-meter/)。

我们喜欢[Dave Marples]量化像 CPU 负载这样复杂的东西的简单方法。他的技术基于这样一个事实，即大多数嵌入式控制器只是无休止地循环等待某件事情去做。通过有策略地设置命令，在 CPU 繁忙时锁存输出，然后在空闲时再次关闭输出，可以产生占空比与 CPU 负载成比例的 PWM 信号。然后，分压器将最大输出调整到 1.0 伏，电容器平滑信号，因此负载由 0 到 1 伏之间的值表示。如何显示负载是您自己的选择；[戴夫]只是用了一个伏特计，但任何从 LED 条到某种音频反馈也可以。

还在为您的台式机寻找负载测量仪吗？随你挑:[一个 LED 矩阵](http://hackaday.com/2013/07/20/led-module-used-to-display-load-traffic-and-status-data-for-your-pc/)、[老式电表](http://hackaday.com/2017/05/13/microcontroller-load-meter-tells-you-how-hard-its-currently-working/)，甚至[德卡龙](http://hackaday.com/2013/07/26/drive-bay-form-factor-dual-dekatron-readouts-for-ram-and-cpu-usage/)。
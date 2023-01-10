# 使固定电压电源可调

> 原文：<https://hackaday.com/2016/05/16/making-a-fixed-voltage-power-supply-adjustable/>

开关模式电源无处不在。多家制造商提供的外形规格一致的标准现成模块。全球化的制造和贸易已经将它们从昂贵的设备变成了商品部件，并且它们很久以前就取代了铁芯变压器，成为需要大电流低压电源时的首选。

[Lindsay Wilson]在工作中遇到了一个电机的电源问题，它需要 7.4V，而在这个电压下找不到现成的电源。他的解决方案是[采用 12V 电源，并将其修改为提供可变电压](http://imajeenyus.com/electronics/20151028_smps_variable_voltage/index.shtml)，这样他就可以拨入他的需求。购买了一个中国制造的 12v 33A 开关电源，他开始工作。

结果，他设计了一个包含旋转电位计的替代反馈分压器，并实现了 5 至 15V 的电压范围。在 PSU 的情况下，安装在它旁边的一个小型 LED 电压表给他一个非常简洁的结果。

修改开关模式电源以提供不同的电压是一条老路[，我们在](http://hackaday.com/2013/07/20/reverse-engineer-a-psu-to-change-its-output-voltage/)之前至少讨论过一次。让 Lindsay 的文章值得一读的是他对 PSU 赛道的逆向工程和详细检查。如果你想了解更多关于开关模式 PSU 设计的各个方面，这是一本详细而可读的入门书。我们建议在你自己打开开关模式 PSU 之前阅读[我们最近关于电源和高压安全的系列](http://hackaday.com/2016/05/11/looking-mains-voltage-in-the-eye-and-surviving-part-1/)，但是即使你永远不会这样做，详细了解它们如何工作也是有所收获的。

这些年来，我们已经在 Hackaday 上几次介绍过[Lindsay]的作品。看看他的[超声波换能器电源](http://hackaday.com/2012/01/30/powering-an-ultrasonic-transducer/)，如果你正在制作我们不久前展示的[超声波烙铁](http://hackaday.com/2016/05/09/an-affordable-ultrasonic-soldering-iron/)，他的[激光剥离带状电缆](http://hackaday.com/2013/11/26/laser-wire-stripping/)，以及他的[打开 USB 隔离器芯片](http://hackaday.com/2014/04/21/whats-inside-a-usb-isolator/)的故事，这可能会有用。
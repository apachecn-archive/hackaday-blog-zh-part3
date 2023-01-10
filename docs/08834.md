# 适合 Arduino 的补偿热电偶放大器

> 原文：<https://hackaday.com/2018/03/15/a-compensated-thermocouple-amp-ready-for-arduino/>

当你想用 Arduino 或其他微控制器测量温度时，有大量传感器可供选择。温度芯片和传感器模块比比皆是，有些内置湿度传感器，所有都易于接口和扩展的支持代码库。但是把其中一个传感器浸入熔融的铝中，你就有问题了。

如果你在测量热的东西，你需要一个热电偶。问题是，热电偶的信号非常小，需要放大和补偿后才能馈入典型微控制器的 ADC。由于找不到满足他需求的商用放大器，【monk Helios】[为微控制器](https://hackaday.io/project/67584-thermocouple-amplifier-for-arduino-and-other-mcu)打造了自己的热电偶放大器。该设计以 LTC2053 仪表放大器为中心，该放大器将 K 型热电偶的 40.6μV/°C 输出转换为精确调整的 10mV/°C 范围，正好适合 ADC 的功耗。他还精心设计了 LT1025 冷结补偿器；热电偶放大器以 0°C 为基准，因此补偿器测量结冷端的实际温度，并相应调整输出。整个放大器很好地布置在 DIY 单面 PCB 上，精心应用了阻焊膜——这是我们很长时间以来见过的最好的家庭蚀刻板之一。

[Bil Herd]不久前自己设计了一个类似的热电偶放大器，所以你也可以看看。或许你需要仪表放大器的基础知识？[我们的“超越测量”系列](http://hackaday.com/2016/03/11/beyond-measure-instrumentation-essentials/)将带你开始。
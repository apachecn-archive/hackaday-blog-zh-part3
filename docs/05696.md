# 你用了多少瓦特？

> 原文：<https://hackaday.com/2017/04/22/how-many-watts-are-you-using/>

最好的智能家居技巧之一是安装某种能源监控器。很容易*说*你在努力节约能源，但是没有确凿的数据，这只是说说而已。此外，这是一个简单而又很棒的方法，可以让全家人都可以自己动手做东西。

[波格丹一世]在周末从零开始建立了一个简单的[全公寓电源监控器](http://bogdan.nimblex.net/diy/2017/04/19/apartment-energy-monitor.html)，他很友好地向我们展示了整个过程，从拿起一个分裂核心 CT 传感器开始，到完成一个项目结束。

他的项目的大脑是一个 ESP8266 模块，这意味着他需要调整 ct 传感器，以输出位于芯片的 ADC 范围 0 V 至 3.3 V 内的电压。如果你正在进行一个能源监控项目，这很容易选择正确的[负载电阻](http://tyler.anairo.com/projects/open-energy-monitor-calculator)值，然后将接地电压上调 1.6 V 左右。我们说这很容易，但是有一个工作示例和一些范围镜头是很好的。微控制器频繁读取 ADC，做一点数学运算，就大功告成了。

其余的代码是从这里或那里借来的。EmonLib 负责数学计算，ArduinoOTA 允许他无线刷新固件， [Blynk](http://hackaday.com/2016/03/10/app-control-with-ease-using-blynk/) 负责制作一个漂亮的 Android 应用程序用于可视化。最终，一个漂亮的点阵 LED 显示屏让[波格丹一世]对他客厅里的每一瓦特都念念不忘。为 ESP8266 增加第二个 ADC 通道，以便他可以通过测量瞬时电压获得更高的精度，这可能是下周末的一个项目。
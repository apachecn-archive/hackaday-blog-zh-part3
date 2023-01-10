# 使用 ESP8266 实现 Wi-Fi 串行遥测

> 原文：<https://hackaday.com/2016/03/04/serial-telemetry-to-wi-fi-with-an-esp8266/>

Hackaday.io 用户[J. M. Hopkins]的火箭技术有问题。火箭的遥测数据通过 433MHz 的串行链路传到地球，但在阳光明媚的日子里，从海量数据中挑选出他需要的数据，供以后在笔记本电脑屏幕上进行分析，变得有点困难。

他的解决方案是[将串行数据从他的收发器模块带到一个 ESP8266](https://hackaday.io/project/9937-70cm-serial-wifi-bridge) ，然后两者通过 WiFi 共享数据，并通过 I2C 将相关信息显示到一个 LCD 上，以便于参考。他把所有的电源都放在一个非常漂亮的木箱里，箱子背面有一个 SMA 插座来连接他的八木。

从遥测技术接收到的所有信息都通过 WiFi 通过 Telnet 连接到客户端，但 LCD 的相关信息是通过从方括号中的火箭发送来选择的。我们希望源代码能及时发布。

这不是我们第一次在 Hackaday 这里[展示](http://hackaday.com/2012/07/16/rocket-telemetry-from-uav-hardware/)火箭[遥测](http://hackaday.com/2011/02/17/model-rocket-radio-telemetry/)。如果我们不指出这个项目使用我们自己的 [Hackaday 品牌 Huzzah ESP8266 分线板](http://store.hackaday.com/products/huzzah)，我们就错过了一个技巧。
# 飞机观察者发现飞机，追踪目的地

> 原文：<https://hackaday.com/2016/07/17/planespotter-spots-planes-tracks-destinations/>

有没有仰望天空，想知道你头顶上的那些飞机要去哪里？多亏了他基于 ESP8266 的[飞机观测器](http://blog.squix.org/2016/07/esp8266-based-plane-spotter-how-to.html)，现在【squix】再也不用这么做了。

他建造了这个漂亮的设备来捕捉他看到的从苏黎世机场起飞的航班的细节。这是一个简洁的构建，运行在从 ADS-B 交换站接收 ADS-B 数据的 ESP8266 上。此服务允许您查询特定位置的 ADS-B 数据。

[squix]的飞机跟踪器向 ADS-B exchange 发送一个查询，询问他所在位置和某个高度以下的航班(这样他就能看到那些刚刚起飞的航班)，然后在有机发光二极管屏幕上显示收到的信息。他说，一个仅显示的版本将花费你大约 20 美元，而完整版本也可以接收并与 ADS-B 交换共享数据，将花费你大约 50 美元。那比飞机票便宜多了…
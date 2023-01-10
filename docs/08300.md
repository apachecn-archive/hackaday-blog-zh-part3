# ESP8266 信标宣布你的到来

> 原文：<https://hackaday.com/2018/01/21/esp8266-beacon-announces-your-arrival/>

过去，人们只要按下汽车上的一个按钮，就能打开车库门，这已经足够幸福了。但是按一个按钮意味着你必须用手，就像它是一个婴儿玩具什么的。我们生活在 21 世纪，肯定有更好的方法！好吧，如果你有一个家庭自动化系统设置和一个备用的 ESP8266，那么[aderusha] [可能有你的 MQTTCarPresence](https://github.com/aderusha/MQTTCarPresence) 解决方案。

这里的操作理论很巧妙。ESP8266 通过仪表板内的 USB 端口供电，该端口随发动机打开和关闭。当引擎启动时，ESP8266 通电并立即连接到 WiFi 网络，并向家庭助理推送 [MQTT 消息。当 Home Assistant 收到 ESP8266 已连接的通知时，它会打开车库门。](https://home-assistant.io/docs/mqtt/discovery/)

当[aderusha]开车离开车库和房子时，ESP8266 会失去与网络的连接，并且家庭助理会关闭车门。当他回家时，同样的原理起作用:当汽车接近房子时，它连接到网络，车库门打开，当发动机在车库中关闭时，门再次关闭。

设置的硬件方面实际上只是一个 WeMos D1 迷你 Pro 板，尽管他添加了一个外部天线，以确保当车辆滚动时信号得到接收。他还设计了一个非常光滑的 3D 打印盒，将所有东西放在一个整洁的小包装中。

我们之前讨论过基于 ESP8266 的自动进入系统，[尽管 ESP 通常呆在家里](https://hackaday.com/2017/06/04/esp8266-mqtt-remote-gate-entry/)。如果你想建立自己的自动化系统，一定要看看[【埃利奥特·威廉姆斯】推出的关于 MQTT](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/) 奇迹的精彩系列。
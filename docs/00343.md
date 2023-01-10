# 通过 ESP8266 将血压数据推送到云端

> 原文：<https://hackaday.com/2015/10/11/push-blood-pressure-data-to-the-cloud-via-esp8266/>

[Eduardo]联系我们，告诉我们他成功地将血压计连接到网络上。他通过定位测量后负责存储血压数据的芯片实现了这一目标。这是一个简单的 I2C EEPROM，他从其中转储数据，并与 4 位逻辑分析仪进行通信。[Eduardo]发表了他在该交流计划中的所有发现，所以请查看他的帖子了解更多信息。要点是他使用 ESP8266 实现了他的逆向工程协议，这是一种无处不在的廉价 WiFi 板，已经成为联网的任何东西的首选，如[电源监控器](https://hackaday.com/2015/10/04/wifi-power-monitor/)和动力不足但[令人敬畏的服务器农场](https://hackaday.com/2015/09/05/esp8266-web-server-farm/)。查看[黑客字典条目](https://hackaday.com/2015/09/24/hackaday-dictionary-the-esp8266/)了解更多信息。

[Eduardo]并不是第一个使用这种设备的人，你可以在亚马逊上看到一个 Withings 设备和一个 T2 blip care 设备。(Eduardo)的这一黑客行为确实提供了一种更廉价的途径来连接来自地理位置遥远、或许有技术恐惧症的家庭成员的重要医疗数据。让我们沿着假设的小路走一走，好吗？阿尔布开克的鲍勃叔叔在当地没有任何家人，他可能是这种被黑客攻击的设备的一个很好的候选人，每个人都知道让老年家庭成员向亲人报告一些健康信息就像拔牙一样……但有了[爱德华多]的黑客，这很简单。将硬件(假设你事先知道登录凭证)嵌入到一个新的 BPM 中，作为礼物送给他，你就大功告成了。

我们还没有看到太多的血压监测黑客，但被称为[“疼痛机器”](http://hackaday.com/2014/09/30/pain-machine-brings-pleasure-too/)的[黑客日奖](https://hackaday.io/prize)中的一个参赛项目包括监测用户的血压。我们还报道了一个有趣的关于[用压电元件](http://hackaday.com/2015/03/19/measuring-heart-rate-with-a-piezo/)监测你的心率的黑客攻击。

下面是[爱德华的]袖口的快速演示。

 <https://www.edusteinhorst.com/wp-content/uploads/2015/09/VID_20150823_123520670.mp4?_=1>

[https://www.edusteinhorst.com/wp-content/uploads/2015/09/VID_20150823_123520670.mp4](https://www.edusteinhorst.com/wp-content/uploads/2015/09/VID_20150823_123520670.mp4)
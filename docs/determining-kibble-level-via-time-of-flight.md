# 通过飞行时间确定粗粒含量

> 原文：<https://hackaday.com/2017/08/26/determining-kibble-level-via-time-of-flight/>

[WTH]正在建造一台[物联网猫咪自动售货机](http://www.whiskeytangohotel.com/2017/08/tof-laser-to-monitor-cat-food-levels.html)。有几个这样的项目漂浮在周围，非常敏感地测量出食物的分量——一些使用螺丝一次分配一定量的食物，一些测量剩余储备的重量。这座建筑绝对不是那样。这种 kitty 食品监测器使用飞行时间传感器来确定料斗中剩余的食物量。[WTH]的喂食器让猫吃它想吃的所有食物，然后当粗粮含量低于一定水平时提醒看守人。

该项目从一个宠物食品分配器开始，它由一个漏斗组成，重力将食物送入食物碗中。当动物吃这些食物时，更多的食物被分配到碗里。盖子上连接着一个 ESP8266，与 Adafruit 飞行时间传感器相连。这报告了以厘米为单位的粗粮水平，对于[WTH]的目的来说已经足够了。传感器数据被记录到 Google Drive 电子表格中，通过 M2X ( [在& T 的 IOT 服务](https://m2x.att.com/)上发布为图表，并通过 [IFTTT](https://ifttt.com/) 发送到【WTH】的智能手表上。

在 Hackaday 上寻找过多的推特、Instagramming 和其他自动喂养猫主人的方式。看看[自动猫喂食器分发 noms，wants cheezburger](http://hackaday.com/2015/11/05/automatic-cat-feeder-dispenses-noms-wants-cheezburger/) ，和一个用层压机部件制成的[猫喂食器](http://hackaday.com/2012/05/06/automatic-cat-feeder-made-with-recycled-laminator-parts/)。
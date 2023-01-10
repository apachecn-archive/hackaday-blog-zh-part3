# 找到来源:WiFi 三角测量

> 原文：<https://hackaday.com/2016/05/29/find-the-source-wifi-trangulation/>

[迈克尔]正在玩他的 ESP8266。偶尔，他会注意到一个 WiFi 接入点出现了他所描述的[“一个讨厌的名字”](https://hackaday.io/project/11611-wifi-triangulation)。也许是对拥有这种接入点的人感到好奇，或者是对他以前纯净的领空被玷污感到愤怒，他决定看看是否能找到有问题的路由器。

[迈克尔]为自己建造了一台[步行机](http://hackaday.com/2016/02/24/quickie-wifi-scanner/)。他的 ESP8266 与一个 GPS 模块一起进入，该模块与 PIC 微控制器接口。这一切都被安置在一个现成的案件与键盘和有机发光二极管屏幕。他带着他的作品在附近进行了一次平静的散步，带着一大堆要整理的数据回家。为了节省时间，他将数据放在 SQL 数据库中，并使用查询进行计算。之后，用 Google Maps API 和一些 JavaScript 快速组装了一个网站，对计算结果进行三角测量。

果然，有问题的 WiFi 接入点的人出现在地图上。
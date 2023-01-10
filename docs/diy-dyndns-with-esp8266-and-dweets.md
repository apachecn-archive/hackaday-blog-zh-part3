# 带 ESP8266 和 Dweets 的 DIY DynDNS

> 原文：<https://hackaday.com/2017/04/12/diy-dyndns-with-esp8266-and-dweets/>

你在家用路由器上，你的 IP 地址一直在变。与其为一个静态的 IP 地址支付额外的费用(并成为互联网的成年成员),有许多服务可以让你动态地将你当前的 IP 地址发布给世界其他地方。但是大部分都涉及到付钱或者花时间看广告。谁有钱或有时间？！

[Alberto Ricci Bitti]将一些免费服务和一个 ESP8266 模块拼凑在一起，制作了一个[设备，该设备偶尔会将其外部 IP 地址推送到基于网络的“dweet”服务](https://github.com/riccibitti/CloudMyIp)。精简版:一台 ESP8266 从 ipify.org 的[获得其外部 IP 地址，并通过](http://ipify.org/)[的 dweet](http://dweet.io/) 将其推送到一个基于网络的数据存储中。 [Freeboard](http://freeboard.io/) 读取“dweet”并以一种漂亮的格式发布结果链接。

这个软件服务短链的每一部分都可以很容易地被其他任何东西取代。上个世纪，当我们还在拨号上网的时候，我们就拼凑出了自己类似的解决方案。但是[Alberto R B]的解决方案既快速又简单，并且使用了不少于三个(3！)云服务以`.io`结尾。将 ESP8266 添加到您想要公开的 WiFi 网络，就大功告成了。
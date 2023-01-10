# CarontePass:为你的黑客空间开放访问控制

> 原文：<https://hackaday.com/2016/04/13/carontepass-open-access-control-for-your-hackerspace/>

随着协作工作空间的发展，所有协作工作空间面临的一个问题是访问控制。你怎样才能让你的会员安全地进入这个空间，而不用承担任何时候都有一个钥匙持有人在现场的费用和不便。

[Torehc]正在加那利群岛特内里费的[Kreitek makers space](http://kreitek.org/)(西班牙语， [Google Translate link](http://translate.google.com/translate?sl=auto&tl=en&u=http%3A%2F%2Fkreitek.org%2F) )用他的 [CarontePass RFID 门禁系统](https://hackaday.io/project/10498-carontepass-open-access-control)解决这个问题。

每扇门都有一个带有 RFID 阅读器的客户端，可以是 Raspberry Pi 或 ESP8266，它通过 WiFi 连接到运行基于 Django 的 REST API 的 Raspberry Pi 2 服务器。该服务器可以访问付费会员及其 RFID 密钥的数据库，因此可以向客户端发出开门命令。该系统还支持电报消息服务，因此可以查询空间是否开放以及在特定时间有多少成员在。

该项目的所有资源[都可以在 GitHub 知识库](https://github.com/torehc/carontepass-v2)上获得，还有一个[项目博客](https://carontepass.wordpress.com/)(西班牙语，[谷歌翻译链接](http://translate.google.com/translate?sl=auto&tl=en&u=https%3A%2F%2Fcarontepass.wordpress.com%2F))提供更多细节。

这是一个仍在积极开发中的项目，[Torehc]承认其安全性需要更多的工作，因此正忙于实现 HTTPS 和更好的访问安全性。目前，我们可以看穿机器翻译的迷雾，它依赖于自己的加密 WiFi 网络的安全性，所以我们倾向于同意他的观点。

这不是我们在这里介绍的第一个黑客空间访问系统。得克萨斯州的 MakerBarn 有一个使用粒子光子的[，而密西根州的兰辛创客网](http://hackaday.com/2015/12/13/maker-barn-organizer-creates-makerspace-access-control-system/)[有一个巧妙的门机制](http://hackaday.com/2013/11/10/rfid-door-access-robot/)，康涅狄格州的 Nesit hacker space[有一个非常奇特的视频反馈系统](http://hackaday.com/2013/04/17/hackerspace-security-system-brings-rfid-video-feedback-and-automatic-doors/)。你的空间是怎么解决这个问题的？

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)
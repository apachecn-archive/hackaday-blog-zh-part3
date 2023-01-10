# Google Home 遇上 ESP8266

> 原文：<https://hackaday.com/2017/05/23/google-home-meets-esp8266/>

[Luc Volders]正在 Google Home 和 ESP-8266 的帮助下建造自己的智能房屋。受电视节目中家用电脑的启发，Eureka [Luc]使用现成设备和开源软件的组合创建了一个物联网生态系统。

如今，有大约一千种方法可以打造一个 DIY 智能家居。所有这些都涉及到设置一个命令接收器(像 Amazon 的 Echo 或 Google Home)、某种云连接和一个终端设备控制器。这对初学者来说会变得复杂。[Luc]的文章很棒，因为他以教程的方式介绍了每一步。他甚至通过使用 BASIC 和 ESP-BASIC 对 [ESP8266 进行编程来简化事情。](http://lucstechblog.blogspot.nl/2017/03/back-to-basic-basic-language-on-esp8266.html)

[Luc]使用 If This Then than(IFTT)作为他的云服务。IFTT 是谷歌云服务和连接到他家 WiFi 网络的 ESP8266 之间的粘合剂。说到这里，[Luc]展示了如何在路由器上设置端口转发，以便所有对端口 8085 的访问都转到 ESP8266。不完全是强有力的安全措施——但这比打开整个家庭网络要好。

你不需要一个真正的谷歌 home 设备来进行这次黑客攻击。你可以用树莓皮打造自己的。一旦设置好了，你就可以做任何事情，从开灯到[给你的草坪浇水](http://hackaday.com/2017/04/13/google-calendar-interface-for-your-internet-of-lawns/)。

 [https://www.youtube.com/embed/jcT65CDOKXQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jcT65CDOKXQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 在大型商店物联网插头中找到 ESP8266

> 原文：<https://hackaday.com/2016/09/23/finding-esp8266-inside-big-box-store-iot-plugs/>

当我们购买新的闪亮玩具时，我们通常会打开它们至少看一眼。[斯科特·吉布森]显然也是如此。他[在 EcoPlug 牌 WiFi 控制的墙壁开关内部发现了一个 ESP8266 模块](http://thegreatgeekery.blogspot.de/2016/02/ecoplug-wifi-switch-hacking.html)。

最初的设备旨在由一个(蹩脚的)应用程序控制。他嗅到了足够多的 UDP 数据包，将开关信号发送到未经修改的设备，但这有什么意思呢？[Scott]通过用他自己的替换 ESP8266 的固件对它进行了升级，现在他有了一个功能更强的远程开关，一个像他的家庭自动化系统的其余部分一样说话的[MQTT](http://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)。

代码并不多——它只是做你认为它会做的事情。这就是开放标准和我们开源硬件黑客社区的魅力所在。人们比以往任何时候都更容易接受不符合自己意愿的商业垃圾，并对其进行“修复”。

还有其他方法来打破家庭自动化蛋。在 ESP8266 方面，我们有[甚至更便宜的产品](http://hackaday.com/2016/07/07/dumbing-down-a-smart-switch/)供你破解，甚至还有[完全 DIY 选项](http://hackaday.com/2015/04/19/switch-mains-power-with-an-esp8266/)。在 ESP8266 之前，公司曾经将[完整的 Linux 路由器放入交换机](http://hackaday.com/2014/11/13/hacking-a-20-wifi-smart-plug/)，如果你能相信的话，它们也是可以被黑客攻击的。但值得称赞的是(斯科特)看到了他所拥有的，并把它变成了他想要的。

 [https://www.youtube.com/embed/8CsT6csr7v4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8CsT6csr7v4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[米洛斯]的提示！
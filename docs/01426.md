# 廉价的 WiFi 插座被刷新；发现使用 ESP8266

> 原文：<https://hackaday.com/2016/02/06/cheap-wifi-outlets-reflashed-found-to-use-esp8266/>

今天市场上有一堆简单的支持 WiFi 的插座，所有这些泡罩包装的好东西似乎都有一个共同点——蹩脚的软件。至少从黑客的角度来看是这样的；似乎总有一些你想做的事情是应用程序不支持的。被困在这个位置上，[scootermcgoober]做了明智的事情，[重组了他的廉价物联网商店](http://thegreatgeekery.blogspot.ca/2016/02/ecoplug-wifi-switch-hacking.html)。

虽然[scooter]的视频是最近的，而且他说他是在家得宝买的插头，但我们无法在附近的任何商店找到它们的销售清单。然而，沃尔玛以微不足道的 15 美元列出了同样的设备,所以这个价格对于重复他的实验来说是合适的。休息后的视频显示了他的拆卸过程，其中找到了所有的主要组件，包括一个神秘的模块，在拆封后发现是一个 ESP8266。管脚被追踪，引线被固定在他的串行转 USB 适配器上，很快新的固件开始闪烁。[scooter]的新应用很简单，但一旦你掌握了关键，还有很多改进的空间。所有的[代码](https://github.com/scottjgibson/esp8266Switch)都在 GitHub 上。

像这样的 WiFi 插座和 WeMo 已经被证明是黑客的沃土。当然，如果你不喜欢泡罩包装，你可以随时[推出自己的 WiFi 插座](http://hackaday.com/2015/02/11/wifi-controlled-power-outlets-with-raspberry-pi/)。

 [https://www.youtube.com/embed/8CsT6csr7v4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8CsT6csr7v4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


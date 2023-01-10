# 快速简单的 NTP 时钟

> 原文：<https://hackaday.com/2017/10/04/quick-and-easy-ntp-clock/>

[Danman]有一台内置有机发光二极管显示器的 ESP32，在安装时钟并试图在其上安装几个 NodeMCU 二进制程序的过程中，他想[他应该尝试推出自己的](https://blog.danman.eu/esp32-ntp-oled-clock/)。

[Danman]使用 PlatformIO 编写代码到他的 ESP。PlatformIO 允许[Danman]浏览 NTP 库并将其加载到他的项目中。找到 NTP 库后，[Danman]写了一点代码，并能够上传到 ESP。上传后,[Danman]注意到有机发光二极管上没有显示任何东西，但这只是为他的有机发光二极管建立图书馆时寻找正确地址的简单问题。最后，[丹曼]创造了一个大字体来显示时间，他的迷你时钟完成了！

很高兴看到有人能够从购买主板到组装演示，而且越来越容易。看看[这款有机发光二极管手表](https://hackaday.com/2013/12/17/stylish-oled-watch-uses-accelerometer-instead-of-buttons/)，还有[这款怀表没有使用 OLED](https://hackaday.com/2016/09/15/hackaday-prize-entry-neopixel-pocket-watch/)，但是看起来还是蛮酷的。
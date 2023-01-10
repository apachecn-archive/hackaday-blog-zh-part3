# 景观照明，也是文本

> 原文：<https://hackaday.com/2016/09/09/landscape-lighting-that-also-texts/>

你当地的五金店或花园供应中心可能有你需要的一切来安装景观照明。有一点不太可能的是，在那种情况下，你钱包里的窟窿比院子里的还要少。即使这样，也可以保证，当你的景观照明不正常时，任何现成的设备都不会给你发短信。【马克】的[景观照明系统有，虽然](https://drkmsmithjr.github.io/LConnect/)！

这种景观照明系统由树莓皮供电，拥有一切可以想象的功能。它可以在日落时打开照明，并在晚上设定的时间或随机时间关闭照明。Pi 提供了一个 web 界面，允许用户进一步控制。Raspberry Pi 还可以监控灯光，并在其中一盏灯熄灭时进行感应。如果有，Pi 使用 Twillo 发送文本消息通知。

我们无法想象在这样的设置中还能包含多少功能。当然，如果你身边没有多余的 Pi，你或许可以设法用一个 ESP8266 或者甚至一个[老式 Arduino](http://hackaday.com/2013/11/15/arduino-astronomic-clock-automates-lights/) 来完成这项工作。
# 智能手机电视遥控器由 Homekit 和 ESP8266 提供

> 原文：<https://hackaday.com/2016/09/16/smartphone-tv-remote-courtesy-of-homekit-and-esp8266/>

天哪，这个从智能手机到电视的遥控器真的让人们明白，在过去十年里，硬件项目已经变得多么简单。我们正在谈论[一个稳压器、红外 LED 和 ESP8266，以便在您的家庭网络上添加电视控制](http://www.instructables.com/id/ESP8266-TV-Remote-for-Homekit/?ALLSTEPS)。黑客的硬件部分是一个自制的双面电路板，它将一个 ESP 与一个 micro-USB 端口，一个将 fom 5 降至 3.3 v 的电压调节器和一个用于传输电视代码的 IR LED 匹配。

让我们坐下来细数让这一切成为可能的幸运。USB 是一种标准，现在可以在大多数电视的背面找到——解决了电源问题。支持 WiFi 的廉价微控制器——检查。无处不在的智能手机和与网络上其他设备通信的既定协议——绝对如此。这是一个不可思议的黑客时代。

电视红外遥控代码有很好的文档记录，使用 Arduino 之类的工具很容易发现——事实上[这个](https://github.com/markszabo/IRremoteESP8266)的 ESP IR 固件是建立在【Ken Shirriff 的】Arduino IR 库之上的。草图的其余部分使它成为局域网上的一个准系统设备，等待发送“tvon”或“tvoff”的连接。在这种情况下，它是一个充当 Homekit 服务器的 Raspberry Pi，但是任何数量的协议都可以用于同一个服务器( [MQTT 任何人](https://hackaday.com/tag/minimal-mqtt/)？).

 [https://www.youtube.com/embed/ySmGesev1mk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ySmGesev1mk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


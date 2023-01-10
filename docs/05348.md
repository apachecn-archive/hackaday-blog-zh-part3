# 使用 WiFiManager 配置 ESP8266 Wifi

> 原文：<https://hackaday.com/2017/03/18/configure-esp8266-wifi-with-wifimanager/>

毫无疑问，ESP8266 使创建小 WiFi 部件变得相当容易。然而，许多项目将接入点细节硬编码到设备中。有一个更好的方法:使用 WiFiManager 库。【Witnessmenow】有[好教程](http://www.instructables.com/id/Avoid-Hard-Coding-WiFi-Credentials-on-Your-ESP8266/)和两分钟视频(下面可以看到)。

如果你只是修修补补，硬编码是没问题的。然而，如果你打算把你的设备送走(或者甚至把它带到某个地方)，你可能不想每次换接入点的时候都要重新编程。如果你打算开发一个商业产品，这个问题会更严重。 [WiFiManager](https://github.com/tzapu/WiFiManager) 做很多商业设备做的事情。它最初看起来像一个接入点。您可以使用电话或其他 WiFi 设备连接到它。然后，您可以通过设置网络 ID、密码等将其配置为加入您的网络。

修改一个硬编码的程序来使用 WiFiManager 并不困难，[Witnessmehow]并排展示了一个普通程序和一个 WiFiManager 示例。然后，他复制并粘贴几行代码，让它工作。

本质上，您需要确保您有以下标题:

```
#include <ESP8266WiFi.h> //ESP8266 Core WiFi Library (you most likely already have this in your sketch)
#include <DNSServer.h> //Local DNS Server used for redirecting all requests to the configuration portal
#include <ESP8266WebServer.h> //Local WebServer used to serve the configuration portal
#include <WiFiManager.h> //https://github.com/tzapu/WiFiManager WiFi Configuration Magic

```

您还需要一些设置:

```
WiFiManager wifiManager;
//first parameter is name of access point, second is the password
wifiManager.autoConnect("AP-NAME", "AP-PASSWORD");

```

如果不想要密码，可以省略。您可以在 GitHub 页面上找到一些其他选项。您也可以从那里安装或使用 Arduino 库管理器。

我们最近在 Blynk 教程中提到过这个库。如果你正在寻找一些好的类似消费者的项目来应用它，那么一个[学习遥控器](https://hackaday.com/2017/02/19/esp8266-basic-sets-up-a-web-remote-in-no-time/)怎么样？

 [https://www.youtube.com/embed/A-P20vC7zq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/A-P20vC7zq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 使用 HomeKit 和 ESP8266 定制 Siri 自动化

> 原文：<https://hackaday.com/2016/01/17/custom-siri-automation-with-homekit-and-esp8266/>

当给你的家庭自动化添加一个设备时，知道从哪里开始总是一件困难的事情。最有可能的是，你已经在做设备端的事情(无论你想自动化什么)，所以如果用户端已经搞清楚了就好了。这就是一个这样的例子。[Aditya Tannu]正在利用苹果 HomeKit 协议的功能，使用 Siri 来控制 ESP8266 连接的设备。

[HomeKit 是来自苹果](https://developer.apple.com/homekit/)的一个框架，使用 Siri 作为系统用户端的语音激活。就像[亚马逊的语音控制自动化](http://hackaday.com/2015/12/26/let-alexa-control-your-life-guide-to-voice-enable-everything/)，这是一个成熟的探索。[Aditya]建立在[HAP-NodeJS 包](https://github.com/KhaosT/HAP-NodeJS)的基础上，该包使用任何可以运行 Node 的东西来实现 HomeKit 附件服务器。

一旦服务器启动并运行(在本例中，在 raspberry Pi 上)，每个连接的设备只需通过 MQTT 进行通信。Arduino IDE 用于对 ESP8266 进行编程，并且有大量的 MQTT 草图可用于此目的。来自[Aditya]的最新的例子是对光纤灯的改进。他添加了一个 ESP8266 板，并用 WS2812 模块替换了库存 led。下面演示的当前版本具有设备的开/关和颜色控制。

 [https://www.youtube.com/embed/xbOEbz2knmQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xbOEbz2knmQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [reddit](https://www.reddit.com/r/arduino/comments/40w7et/philips_hue_fiber_optic_light_using_esp8266/)
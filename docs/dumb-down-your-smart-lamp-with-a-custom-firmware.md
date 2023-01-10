# 用定制固件让你的小米智能灯变傻

> 原文：<https://hackaday.com/2018/03/29/dumb-down-your-smart-lamp-with-a-custom-firmware/>

毫无疑问，ESP8266 最大的卖点是其 WiFi 功能，价格低得离谱。偏执的人可能会等待它的闭源固件位在一个巨大的僵尸网络中反人类的那一天，但在那之前，爱好者和商业供应商等将继续把它们放在他们的物联网项目和设备中。其中一个设备是 Yeelight 台灯，你可以通过手机应用程序设置它的色温和亮度。

[fvollmer]获得了这样一个灯，虽然他欣赏它的设计和一般概念，但他不高兴它与外部服务器通信。所以他做了唯一合理的事情，写了他自己的固件，类似于最初的功能，但是省略了 WiFi 部分。毕竟，ESP8266 在其核心本质上仍有很多可提供的:一个成熟的 32 位微控制器，支持最常见的、业余爱好者友好的 SDK。

灯的色温和亮度由旋转编码器/按钮组合开关设置，led 本身通过 PWM 控制。总的来说，这是一项相当简单的工作，为此[fvollmer]选择了[独立的 C SDK](https://github.com/pfalcon/esp-open-sdk) 。最后，[他并没有不合理的谨慎来控制他的家庭用品](https://hackaday.com/2017/12/26/the-bedside-light-app-that-phones-home/)。
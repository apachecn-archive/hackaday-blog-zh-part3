# 将 Esp 用作串行适配器

> 原文：<https://hackaday.com/2015/10/23/use-the-esp-as-a-serial-adapter/>

硬件黑客工具箱中最有用的工具之一是 USB 转串行适配器。有了它，你可以给路由器刷新新的固件，并在嵌入式硬件的二进制海洋中穿梭。USB 转串行适配器的常见形式是 FTDI 分线板。然而，这需要驱动程序，实际上有一个更简单的无线解决方案:[ESP8266 WiFi 模块](http://www.zoobab.com/esp8266-serial2wifi-bridge)。

尽管是目前最好的小型物联网设备，ESP8266 最初是作为 USB 到 WiFi 适配器而设计的。在我们匆忙建造 [WiFi throwies](http://hackaday.com/2015/05/03/esp8266-wifi-throwies/) 、 [WiFi blinkies](http://hackaday.com/2015/09/12/led-ring-around-the-esp8266/) 和怪异的 [WiFi 服务器农场](http://hackaday.com/2015/09/05/esp8266-web-server-farm/)时，我们似乎忘记了将 3.3V TTL 转换为 WiFi 连接的设备仍然有其用途。它是用新固件刷新廉价 WiFI 路由器的完美设备，或者只是为您提供无线串行连接以配合您的无线互联网。

该项目为 ESP8266 使用了 [jeelabs 的 ESP-link 固件。它是 WiFi 和串行之间的一个简单的桥梁，在必要时可以充当 AVR 程序员。这个固件的 web 界面很好看，但是你真的不需要；这个固件的全部目的是比 FTDI USB 转串行适配器更加透明。下一次你用 OpenWRT 刷新路由器时，不要费事去挖 USB 适配器；你只需要一个 ESP。](https://github.com/jeelabs/esp-link)
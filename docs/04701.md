# 车库开门器记录到 Google Drive

> 原文：<https://hackaday.com/2017/01/15/garage-door-opener-logs-to-google-drive/>

车库开门器是这一带非常经典的黑客技术。红外、蓝牙、WiFi、智能手机控制、网络界面——我们都见过。但是如果你想跟踪进出的人，你需要某种方式来记录正在发生的事情。您可以继续下去，推出自己的基于 SQL 的解决方案，绑定到自定义网页中。但是有一个更简单的方法。你可以[制作一个车库开门器，将事件记录到 Google Drive](http://www.whiskeytangohotel.com/2017/01/esp8266-wifi-garage-door-opener-from.html) 。

[WhiskeyTangoHotel]正在寻找一个 ESP8266 项目，一个车库门开启器似乎正是合适的人选。编写代码很简单，对 WiFi 的控制也很方便。与车库门的接口非常简单——现有的开启器使用一个简单的按钮，很容易通过连接继电器来控制。日志记录就像让 ESP8266 向 IFTTT 发送请求一样简单，if TTT 用于向 Google Sheet 发布状态更新。

这个项目相当基础，但还有扩展的空间。通过在 IFTTT 上使用单独的制造商通道触发器，可以跟踪车库门的不同用户。添加一些限位开关或其他传感器来检测门的位置也很容易，因此可以确定门是打开的还是关闭的。

车库门开启器总是有另一个版本——看看这个黑客[响应闪烁的车头灯](https://hackaday.com/2015/04/08/blink-thrice-to-let-me-in/)打开车库门。
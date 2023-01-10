# 从任何地方监控串行端口

> 原文：<https://hackaday.com/2016/03/07/monitor-a-serial-port-from-anywhere/>

这个简单的 [WiFi 串口监控器](https://hackaday.io/project/5680-hardware-serial-port-monitor-with-wifi)本来可以省去我们很多麻烦。我们已经数不清有多少次，仅仅是为了把串口取出来而被连接到一个带有 USB 接口的 Arduino 上，几乎是得不偿失。有时候，我们盘腿坐在地板上，可以选择舒适，也可以选择不小心移动设置，破坏一切，但不能两者兼得。

[弗伦基]的设置简单而巧妙。Ardunio 的串行输出连接到一个 ESP8266。Arduino 以通常的方式向 ESP8266 发送串行消息。然后，ESP8266 将所有这些通过管道传输到一个简单的 JavaScript 网页。使用您家中的任何设备连接到 ESP8266 的 IP，并获得所有串行数据的实时流。干净利落。

这项技术非常简单，我们可以用 TX、RX、GND 和 VCC 螺丝端子制作一个小巧的盒子，将我们从仅仅为了一个简单的测试而拴在水泥地板上的噩梦中解放出来。休息后的视频。

 [https://www.youtube.com/embed/G-3tcZbZII4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G-3tcZbZII4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


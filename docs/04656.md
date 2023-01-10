# 用 ESP8266 追踪飞机

> 原文：<https://hackaday.com/2017/01/07/tracking-planes-with-an-esp8266/>

虽然有显示飞机位置的应用程序，但[squix]想要建立一个专门的飞机定位设备。[ESP8266 planespoter Color](https://blog.squix.org/2017/01/esp8266-planespotter-color.html)是一款独立设备，可在彩色 TFT 屏幕上显示带有平面数据的实时地图。这个设备扩展了他的[飞机观察者](http://hackaday.com/2016/07/17/planespotter-spots-planes-tracks-destinations/)项目，增加了彩色显示和绘图功能。

首先，这个设备需要知道飞机在哪里。从飞机上传输的 [ADS-B](https://en.wikipedia.org/wiki/Automatic_dependent_surveillance_%E2%80%93_broadcast) 数据包含有用的数据，包括高度、速度、位置和飞机独有的标识符。虽然商业服务可以获取这些数据，但飞机观察者使用 [ADS-B 交换](https://www.adsbexchange.com/)。你可以[设置一个树莓 Pi](http://hackaday.com/2014/08/25/piaware-automated-airliner-tracking-on-the-raspberry-pi/) 来记录这个数据，[提供给 ADS-B 交易所](https://www.adsbexchange.com/how-to-feed/)。

随着从 ADS-B 交换 API 接收到平面数据，是时候绘制到屏幕上了。用于 ESP8266 的 [JPEGsDecoder fork](https://github.com/fredericplante/JPEGDecoder) 用于绘制图像，这些图像以 JPEG 格式从 MapQuest API 获取。

最后，需要地理定位来确定飞机观察者的位置。[squix]没有添加 GPS 模块，而是采用了一种廉价的解决方案:WiFi 地理定位。这使用来自附近 WiFi 接入点的识别信息和信号强度来确定位置。这个项目使用[一个【Alexander Mylnikov】的公共 API](https://www.mylnikov.org/archives/1170) ，它返回一个带有经度和纬度的 JSON 对象。

这个项目展示了 ESP8266 的能力，并汇集了一些巧妙的技术。如果你想在 ESP8266 上进行地理定位或显示地图，可以在 Github 上找到代码[。](https://github.com/squix78/esp8266-plane-spotter-color)

 [https://www.youtube.com/embed/4pTkoMsl1H4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4pTkoMsl1H4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


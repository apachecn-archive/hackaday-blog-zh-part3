# Mc 照明消除了眨眼的痛苦

> 原文：<https://hackaday.com/2018/04/14/mc-lighting-takes-the-pain-out-of-blinking/>

如果你想通过 WiFi 闪烁大量类似 WS2812 的 LED 像素，硬件方面的事情很简单:一个 LED 灯条，ESP8266 单元，以及足够强大的电源来供电。但是软件方面——这可能会有点麻烦。

进入 [Mc 灯光](https://hackaday.io/project/122568-mc-lighting)。它使软件方面的事情变得很简单。将固件闪存到 ESP8266 上，您可以选择 REST、WebSockets 或 MQTT 来获取数据。这意味着它可以与 Homekit、NodeRed 或 ESP 托管的 web 界面配合使用，您可以从任何智能手机上下载这些界面。

网页界面特别棒，内置了一堆动画。(查看下面的视频。)这意味着你可以焊接一些电线，闪一闪静电，你最不懂电脑的亲戚可以马上控制系统。说到视频，Mc Lighting 的作者[Tobias]汇编了一个使用该库的项目播放列表，也在下面。GitHub 上的文档很棒，也可以看看 T2 的维基。

你还在等什么？你或你爱的人在生活中需要一些眨眼吗？当你订购 LED 灯带时，买两个。你会想要发出鼻音！也是。

 [https://www.youtube.com/embed/CXfSL81GvQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CXfSL81GvQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/3TUjszkS3bY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PL3RrveYYJCuRDhrZXcRSQgtsIZ2lH64bv](https://www.youtube.com/embed/3TUjszkS3bY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PL3RrveYYJCuRDhrZXcRSQgtsIZ2lH64bv)
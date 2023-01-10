# Pebble 智能手表的留声机

> 原文：<https://hackaday.com/2015/09/13/a-gramophone-for-your-pebble-smart-watch/>

在最近一次以 Pebble 为主题的黑客马拉松上，其中一个团队创造了一个非常酷的设备，叫做 [TimeDock Sleepeasy。](https://www.hackster.io/team-engineerable/timedock-speakeasy)

这是一个受留声机启发的扩展坞，可用于您的 Pebble Time 智能手表。它不仅仅是一个 3D 打印的底座——不，里面有一个 Arduino！该团队从一开始就计划为 Pebble 制作一个交互式坞站，让它可以与你交谈，而无需实际按下手表上的任何按钮。

让 Arduino Uno 与 Pebble 对话是相当棘手的，但一旦他们发现这一点，他们就有了很多交互选项——他们最终使用了一个超声波传感器，所以你只需在 TimeDock 上挥挥手，它就会告诉你时间。

他们如何设置两个设备进行通信，这有点有趣。Arduino 向 Pebble 发送时间请求，Pebble 回复时间和说出时间的请求。团队预装了一堆。WAV 文件，用于 Pebble 上的各种其他通知——当 Arduino 看到它是什么类型的通知时，它会播放相应的。WAV 文件。

 [https://www.youtube.com/embed/qioFUrdXQFE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qioFUrdXQFE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



整个黑客马拉松都是关于利用新发布的 Pebble Time 手表所具有的[智能表带接口](http://developer.getpebble.com/guides/hardware/)-基本概念是利用这一新硬件，你可以设计和制造自己的*智能表带*来为你的智能手表添加额外的功能-如心率传感器、GPS 等。不完全开源——但是正在实现！现在，您可以开发自己的应用程序…和硬件！
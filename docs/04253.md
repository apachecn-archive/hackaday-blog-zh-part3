# 构建自己的 YouTube 播放按钮

> 原文：<https://hackaday.com/2016/11/29/build-your-own-youtube-play-button/>

这个世界上唯一重要的是你在社交媒体平台上获得的喜欢。为此，YouTube 一直在向最有价值的创作者发送银和金播放按钮。[Sean]在玩《我的世界》的时候还没有对着麦克风尖叫足够长的时间来获得这些播放按钮中的一个，[所以他决定自己制作一个](https://hackaday.io/project/18471-arduino-youtube-play-button)。

这个播放按钮不仅仅是 Audible dot com 带给你的一个框架中的一点金属；这个 YouTube 播放按钮实际上做了一些有用的事情。这是一块由 144 个发光二极管组成的印刷电路板，一起作为显示器。板上有一个 Atmel SAMD21 微控制器来驱动 led，还有一个 ESP8266 从互联网上下载数据。什么样的数据值得放在一个 Arduinofied 化的 YouTube 播放按钮上？当然是[【肖恩】的频道](https://www.youtube.com/channel/UCE-bw6PRKuDlH6fP1mP4nOw)的订户数。去订阅吧，可能会让他的播放键崩溃。

不可否认，这个播放按钮 PCB 有一些问题。首先，ESP8266 不能直接与 YouTube API 通信来降低订阅数。这个问题已经用一个可以连接到 API 的 Raspberry Pi 解决了，并对 ESP 进行编程以从 Pi 中提取数据。其次，这是[Sean]第一次对在烤箱中回流焊的双面 SMD 板进行实验。第一面的组装很容易，但是为了安装第二面，[Sean]转向了低温铋焊膏。除了组装电路板时的一个小错误，一切都按计划进行。

这是一个伟大的项目，如果你想看看 YouTube 更好的部分是什么样的，请查看下面的[Sean]视频。不要忘记评价、评论、喜欢、不喜欢或订阅。

 [https://www.youtube.com/embed/IK88ALh8d5w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IK88ALh8d5w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


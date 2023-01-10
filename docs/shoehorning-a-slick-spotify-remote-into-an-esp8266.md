# 把一个光滑的 Spotify 遥控器塞进 ESP8266

> 原文：<https://hackaday.com/2018/07/11/shoehorning-a-slick-spotify-remote-into-an-esp8266/>

2017 年，Spotify 最终弃用了他们的公共香草 C SDK 库 libspotify，并正式用 iOS 和 Android 专用 SDK 以及我们都听说过的这种新的网络事物取代了它。这对它们的可维护性来说可能很好，但是这使得为 Linux 或硬件设备编写本机应用程序变得非常困难，至少在没有应用程序进程和 NDA 的情况下是如此。或者是？[Dani]希望构建一个方便的“正在播放”显示和远程控制界面，而不是使用他们口袋中无聊的玻璃和金属平板，但受到上述 SDK 限制的约束。因此，他们想出了一系列聪明的优化措施，产生了名副其实的 [ESP8266 Spotify 遥控器](https://thingpulse.com/the-esp8266-spotify-remote-engineering-challenges/)。

Spotify 遥控器有一个带触摸屏的彩色 LCD。一旦附加到 Spotify 帐户，它将显示当前播放曲目的专辑封面(带有加载指示器！)并允许您在触摸屏上播放/暂停/跳过曲目，所有这些都具有令人印象深刻的低延迟。为了实现这一目标，[Dani]面临两大挑战:授权 ESP 与用户的 Spotify 帐户进行交互，以及低延迟 LCD 绘图。

![](img/f711648da70e6e4c902fa5f30c499dca.png)

2 Bit Cover Art

如果你不在 iOS 或 Android 上，Spotify web API 是剩余的非 NDA 界面。但它实际上是为在相对丰富的平台上使用而设计的，比如全功能的网络浏览器，而不是嵌入式设备。为此，要求用户在静态登录框中输入用户名和密码的日子已经一去不复返了，更新(更好)的方法是协商每个用户的令牌(每个应用程序单独授权)，然后使用它来验证您的交互。在这种情况下，第三方应用程序(在这种情况下是 ESP8266)永远看不到用户的密码。这一过程的一个已被编纂且非常常见的版本被称为 [OAuth](https://oauth.net/) ，令牌舞被称为“工作流”。如果你想了解这个理论的更多细节，Dani 在他们的帖子里有一篇关于这个过程的很好的文章。在敲出 web 请求和异常处理(用户拒绝授权设备，等等)之后，最后的魔法是使用 [mDNS](https://en.wikipedia.org/wiki/Multicast_DNS) 让用户的浏览器将自己重定向到 ESP 的本地 web 服务器，而无需先查找 IP。因此，设置过程是这样的:ESP 启动并显示一个 URL，用户在 WiFi 连接的设备上导航到那里并运行授权工作流，然后交换令牌并授权远程控制。

第二个问题是平滑绘图。按照 ESP 的标准，给定音轨的全色深专辑封面的存储量相当大，这意味着传输到显示器的速度很慢，并且需要大量内存。[Dani]在这里用了一些技巧。第一个是尝试 2 位色深，结果很糟糕(见上图)。最终，解决方案变成仅当轨道改变时，解压缩并直接将专辑封面绘制到屏幕上(而不是帧缓冲区)，然后用 2 位颜色快速重绘传输控件。最后一个问题是网络传输*也*慢，需要在下载代码和显示绘图路由之间手动[分时](https://en.wikipedia.org/wiki/Time-sharing)以确保每样东西都被频繁重绘。

休息过后，看看[Dani]的视频，看一眼[来源](https://github.com/ThingPulse/esp8266-spotify-remote/)，尝试自己制作一个 Spotify 遥控器。

 [https://www.youtube.com/embed/xKmXMUoo8ps?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xKmXMUoo8ps?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


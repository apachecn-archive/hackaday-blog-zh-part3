# 全球热核战争:推特

> 原文：<https://hackaday.com/2017/10/08/connecting-a-50-geiger-counter/>

安德烈亚斯·斯皮斯今年早些时候做了一个关于核辐射避难所的视频。所以现在他有兴趣将盖革计数器连接到网络上是有道理的。他娶了一个带 ESP32 的预制柜台。如果只是这么简单，那就不会非常引人注目了，但[Andreas]也对计数器的原理图进行了逆向工程，并讨论了操作理论。你可以在下面看到完整的视频。

我们经常认为我们不需要联网的烙铁或烤面包机。然而，如果你有一个辐射事件，得到一个手机警报实际上可能是有用的。当然，如果这一事件是第三次世界大战的开始，你可能不会得到警告，但反应堆气体泄漏或类似的事情可能会使这 50 美元物有所值。

[Andreas]从 GitHub 的软件开始，该软件将电路板与 Arduino 接口。他使用一个免费的 Thingspeak 账户在网络上拍摄数据。IFTTT 可以从 Thingspeak 获取数据，然后向你的手机发送通知。

如果 50 美元超出了你的预算，我们已经看到了[更便宜的版本](https://hackaday.com/2017/01/18/a-no-solder-scrap-bin-geiger-counter-for-15/)。一旦你有了电子管，你真的只需要一些高电压，你真正需要的是一个 555 和一个变压器。

 [https://www.youtube.com/embed/K28Az3-gV7E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K28Az3-gV7E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


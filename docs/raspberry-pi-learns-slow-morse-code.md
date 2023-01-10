# 树莓 Pi 学习慢速莫尔斯电码

> 原文：<https://hackaday.com/2017/11/13/raspberry-pi-learns-slow-morse-code/>

不久前，你需要知道莫尔斯电码才能成为业余无线电爱好者。这个需求在大多数地方都已经消失了，但是代码仍然是有用的，许多火腿使用它，尤其是喜欢黑客的火腿。现在，hams 正在使用 Raspberry Pi 以极低的功耗接收高可读性的莫尔斯电码。该软件名为 QrssPiG，可以处理音频或使用廉价的 SDR 加密狗。

代码的性能优于语音和许多其他模式有几个原因。首先，为莫尔斯制造发射机非常简单。此外，即使在恶劣的条件下，莫尔斯电码也是高度可读的。这部分是因为它的带宽非常窄，部分是因为你的大脑是一个惊人的信号处理器。

像大多数通信方式一样，你走得越慢，信号就越容易通过。在业余无线电爱好者的说法中，QRS 的意思是“发送得慢一点”，所以 QRSS 的意思是“发送得非常慢”。所以火腿使用非常慢的代码，用计算机化的方法监听它。由于数据速率非常低，计算机有时间采取极端的方法来恢复信号——本质上，它可以采用极窄的滤波器。在世界范围内，从一个远小于一瓦的发射机中检测到 QRSS 信号是很常见的。你可以从下面的[K6BFA]和[KI4WKZ]中看到该模式的视频介绍。

那么多慢才算慢呢？例如，[VA3LK]信标每 90 秒发送一个元素，而不是一个单词或字符！这大约是每分钟 0.013 个单词，并且支持大约 0.033Hz 的滤波器带宽。这比常规莫尔斯电码操作中使用的最锐利的过滤器还要窄得多。

通常的做法是对 QRSS 采用频移键控(FSK)。在这个方案中，点和划长度相同，但频率略有不同。人们不会听这些信号，因为它们慢得令人沮丧。它们可以在软件中加速(当然是在你收到它们之后)，但大多数人都是从屏幕上直观地阅读或者用软件解码。

在使用个人电脑之前，我们已经了解了 QRSS。在一个无头的 Raspberry Pi 上有一个接收器将使构建自动化接收器或其他非用户应用程序变得更加容易。我们之前也看过[树莓派的《送 QRSS》](https://hackaday.com/2013/01/25/raspberry-pi-used-as-a-beacon-transmitter/)。

 [https://www.youtube.com/embed/m8tJz6oNGSc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m8tJz6oNGSc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


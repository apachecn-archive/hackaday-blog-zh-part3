# 基于网络的调制解调器

> 原文：<https://hackaday.com/2017/10/18/a-web-based-modem/>

如果你超过了一定的年龄，你会记得在上网之前有奇怪的嗡嗡声和嘎嘎声。调制解调器使用音调通过普通电话线传输和接收数据。有很多技巧用来保持调制解调器的速度，直到最后，你可以下载(但不是上传)到惊人的每秒 56，000 比特。马丁·柯克霍尔特·梅尔胡斯决定[再造一个调制解调器](https://martinmelhus.com/web-audio-modem/)。在网络浏览器中。不开玩笑。

我们开始谈论云中的调制解调器，但这并不准确。调制解调器使用 HTML 5 音频 API，所以它真正地在浏览器中运行。如果[Martin]发明了一种能够与真正的调制解调器进行交互的调制解调器，我们会感到非常惊讶，但是正如您所料，浏览器调制解调器只能与自身的其他实例进行通信。如果你想简单了解 HTML 5 音频，你可能会喜欢下面的视频。

尽管如此，这项工作令人印象深刻，如果你看看 GitHub 上的代码，它并没有你想象的那么复杂。你也可以看看[的现场演示](https://martme.github.io/webaudio-modem/)。这些音调让我们想起了业余无线电爱好者使用的一些多音编码，比如 MFSK。

虽然这对大多数人来说可能没有太大的实用价值，但它确实让我们思考。一台带有扬声器的安全的空气隙计算机可以使用类似的东西广播数据，而不仅仅是一个网页漏洞。我们想知道你是否能把音调调得足够高，让大多数人听不到？如果你想用一侧的 Arduino 来完成类似的把戏，你可以。

我们讲述了[调制解调器技术如何推动现代电话的发展。当然，如今，调制解调器比电话线更有可能将](https://hackaday.com/2016/08/16/retrotechtacular-tom-carter-revolutionized-your-phone/)[连接到互联网。](https://hackaday.com/2017/10/07/retromodem-for-the-commodore-64/)

 [https://www.youtube.com/embed/xmGv_Schm5U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xmGv_Schm5U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 秘密听电梯音乐

> 原文：<https://hackaday.com/2016/05/24/secret-listening-to-elevator-music/>

虽然我们不认为这是一次“失败”，但它肯定不是一次胜利。但这就是当你注意到一些有趣的事情并开始调查时会发生的事情:如果你幸运的话，它会以“找到了！”，但大多数时候只是“哦”一声。不过，记录下“ohs”还是不错的。

约尔特拉克勒在一家酒店呆得太久了，他厌倦了，于是[开始像你一样在网络](http://wiki.gkbrk.com/Hotel_Music.html)中四处窥探。在破解 Wireshark 之后，他注意到一个非标准端口上有很多 [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol) 流量，所以他想看一看。

几个快速的 Python 脚本之后，他下载了一些样本包，将它们解码成十六进制，并找到了 LAME(一个 MP3 编码器)的签名。他调整了字节偏移量，直到得到一个有效的 MP3 文件，瞧，神奇的发现！这是酒店电梯里的音乐流——他在外面的走廊里就能听到，不费吹灰之力。([悲伤长号](https://www.sadtrombone.com/))。)

但是这次什么都没有出现并不意味着下次什么都没有出现。当你真正需要技能的时候，保持技能的锋利是很重要的。我们喜欢跟随人们的逆向工程努力，不管他们最终是否有所发现。你最近发现了什么奇怪的信号？

谢谢[莱昂纳多]的提示！Wireshark 图片来自 Wireshark 上 [Softpedia 的](http://linux.softpedia.com/get/Internet/HTTP-WWW-/Ethereal-1961.shtml)条目。[Oona[windy tan]ris nen 的模拟荧光音频显示器](http://www.windytan.com/2013/03/rendering-pcm-with-simulated-phosphor.html)(看看这个！).
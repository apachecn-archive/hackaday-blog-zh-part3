# Linux 的语音识别更近了一步

> 原文：<https://hackaday.com/2018/01/17/speech-recognition-for-linux-gets-a-little-closer/>

对着一个小盒子大喊命令并让它回答你已经变得很平常了。然而，桌面语音输入从未真正成为主流。对于选择极其有限的 Linux 用户来说，这尤其缓慢，尽管最近版本的 Windows 和 OS X Yosemite 以及更高版本的操作系统都内置了不错的语音支持。

有四个著名的开放语音识别引擎:CMU 斯芬克斯、朱利叶斯、卡尔迪和最近发布的 Mozilla 的 DeepSpeech(他们共同语音倡议的一部分)。Linux 用户的诀窍是成功地设置它们并在应用程序中使用它们。[迈克尔·谢尔登]的目标是解决这个问题——至少对 DeepSpeech 来说是这样。他创建了一个 IBus 插件[，让 DeepSpeech 可以与几乎任何 X 应用](http://blog.mikeasoft.com/2017/12/30/speech-recognition-mozillas-deepspeech-gstreamer-and-ibus/)一起工作。他还提供了 PPAs，这使得安装 Ubuntu 或相关发行版变得容易。

你可以在下面的视频中看到这是可行的，尽管[迈克尔]承认这只是一个起点。然而，开源的伟大之处在于，有了一个工作平台，其他人可以很容易地做出贡献，并在他已经开始的工作基础上进行构建。

IBus 是 Linux 中你不常想到的部分之一。它从程序中抽象出输入设备，主要是为了适应不适合字母数字键盘的输入方法。通常是日语、中文、韩语和其他非拉丁语言。然而，没有理由 IBus 不能处理语音。

奇怪的是，你将看到的 Linux 计算机处理语音输入的最常见方式是将其捆绑起来，并将其发送给像谷歌这样的人进行翻译，尽管有足够的马力在本地处理事情。如果你对灵活性不太挑剔，[即使是 Arduino 也能做到](https://hackaday.com/2013/12/31/an-arduino-with-better-speech-recognition-than-siri/)。随着所有针对神经网络的[最新工具](https://hackaday.com/2017/03/24/ten-minute-tensorflow-speech-recognition/)，语音识别算法不再是一个大问题，而是找到一个足够广泛的训练数据库，然后将数据与其他应用程序集成。这个 IBus 插件解决了最后一个问题。

 [https://www.youtube.com/embed/Kjos5s0ZZDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Kjos5s0ZZDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


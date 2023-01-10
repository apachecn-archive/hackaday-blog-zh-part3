# 看看是谁打来的

> 原文：<https://hackaday.com/2015/10/11/see-whos-calling-with-caller-pi-d/>

生活中最难的事情之一是看着你的父母变老。当他们的感官失效时，最简单的事情对他们来说变得困难甚至不可能。

[基普]的妈妈正在慢慢失去她的视力。因此，她很难看到来电显示上的读数。当然，她可以买到很多具有文本到语音转换功能的设备和手机，但这些设备上的音频通常很混乱。是的，智能手机本身可以显示打电话的人的照片，但[kjepper]的妈妈并不精通技术，也不需要智能手机自带的其他东西。她需要的是[一个非常简单的界面，可以清楚地知道谁在呼叫](http://imgur.com/a/hdMCg)。

最初，[kjepper]试图只使用 USB 调制解调器来捕获来电显示数据。但不管是什么原因，直到他在调制解调器和 Pi 之间添加了一个[FSK](https://en.wikipedia.org/wiki/Frequency-shift_keying)–[DTMF](https://en.wikipedia.org/wiki/Dual-tone_multi-frequency_signaling)转换器，它才开始工作。他编写了 [some Node.js](https://github.com/kjepper/CallerPi) 以便与 Pi 通信，并将信息发送到屏幕上，屏幕可以同时显示多达四个呼叫。为了制作一个对妈妈友好的界面，他把一个旧的光电鼠标拆成滚轮，用木头包起来。妈妈可以旋转滚轮将系统从待机状态唤醒，点击它将来电标记为已读。现在，每当朱迪阿姨打电话给座机时，很明显是她而不是某个电话推销员。

[通过 [r/DIY](https://www.reddit.com/r/DIY/comments/3nls9m/callerid_for_the_visually_impaired/)
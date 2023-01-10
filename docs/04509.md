# 黑掉 Google Daydream 来和 IOS 一起工作

> 原文：<https://hackaday.com/2016/12/20/hacking-google-daydream-to-work-with-ios/>

谷歌白日梦是一个带控制器的虚拟现实耳机，据谷歌的人说，“它目前不兼容 iOS，可能几年内都不会兼容。”好的。

这启发了 Matteo Pisani 开始研究它与 Android 手机对话的协议。开门见山，他在几天内就把它修好了。

真的没有什么大不了的。控制器通过蓝牙发送数据，[Matteo]注意到网络上有一个“未知”设备。从它发送的数据来看，当他移动控制器时，数据发生了变化。现在不那么不知道了！剩下的工作包括编写应用程序来测试假设，挥动控制器，并找出他是否正确。如果你有兴趣自己实现它，请仔细阅读。

我们喜欢这里的礼仪。从[在你自己的遥控器上运行四轴飞行器](http://hackaday.com/2016/06/28/reverse-engineering-quadcopter-protocols/)，到简单的[试图打开灯泡](http://hackaday.com/2016/01/16/shmoocon-2016-z-wave-protocol-hacked-with-sdr/)，理解我们的设备所说的各种语言变得越来越重要。
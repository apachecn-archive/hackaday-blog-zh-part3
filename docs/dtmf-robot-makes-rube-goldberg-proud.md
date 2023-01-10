# DTMF 机器人让鲁贝·戈德堡骄傲

> 原文：<https://hackaday.com/2016/05/27/dtmf-robot-makes-rube-goldberg-proud/>

有时你开始构建，项目会发展。一层又一层的功能累积、增长，否则只会堆积起来。或者至少我们猜测这就是[Varun Kumar]的由 DTMF 控制的 sweet "[监视车所发生的事情。](http://www.engineersgarage.com/contribution/surveillance-car-controlled-dtmf?page=1)

如果你从未深入研究过并不古老的电话技术，那么[双音多频](https://en.wikipedia.org/wiki/Dtmf)信号是老式按键式电话的工作原理。如你所想，DTMF 通过一次播放两个音高来对音频数据进行编码。通过使用一个矩阵，8 个音调被映射到 16 个数字，这个矩阵看起来不像老式电话键盘(但是有一个额外的列)。一个间距对应一列，一个间距对应一行。找出正在播放的音调，你就解码了信号。

无论如何，你可以在易贝花几分钱买到 DTMF 解码芯片，它们为一个简单的机器人提供了一个很好的远程控制接口，这大概就是[Varun]如何开始的。然后他决定他需要机器人上的手机通过 WiFi 发回视频，并意识到他也可以将手机用作遥控器。所以他下载了一个双音多频音发生器应用程序到手机上，然后他就可以控制 VNC 了。[GitHub 上的详细信息](https://github.com/varun13169/Engineers_Garage/tree/master/Surveillance%20Car%20Controlled%20via%20DTMF)。

是的，没错:无线 VNC 控制手机上的一个应用程序，它从音频插孔发出两个音调，由 DTMF IC 解码，然后(并行)二进制输出被输入到 Arduino，作为机器人的大脑。

最后，它看起来像是鲁布-戈德伯格式的，但是使用手机的音频输出作为控制信号实际上是非常聪明的。毕竟，手机到 Arduino 的接口是棘手的部分。DTMF 是一个容易使用的标准，它避免了 USB 或蓝牙设备的麻烦。

我们爱 DTMF。有了 16 个信号，它比堪萨斯城磁带标准和衍生标准要酷得多，而且有一个完整的(现在已经部分废弃)基础设施围绕着它建立。带上双音多频黑客！

 [https://www.youtube.com/embed/ecWZbtY6rOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ecWZbtY6rOI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


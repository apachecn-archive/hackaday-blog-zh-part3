# 谷歌 AIY:人工智能你自己

> 原文：<https://hackaday.com/2017/05/04/google-aiy-artificial-intelligence-yourself/>

当亚马逊向他们的语音服务 Alexa 发布 API 时，他们基本上迫使该领域的任何严肃玩家也将他们的产品带入黑客/制造商市场。现在谷歌和 Raspberry Pi 联手给我们带来了“人工智能你自己”或 AIY。

谷歌制作的免费硬件套件与 MagPi 杂志的第 57 期[一起分发，该杂志面向制造商和爱好者，你可以在休息后的视频中看到。该套件包含一个树莓 Pi 语音帽，一个麦克风板，一个扬声器和一些小零件，以将该套件安装在树莓 Pi 3 上。将所有这些放在一起，并按照官方网站](https://www.raspberrypi.org/blog/free-aiy-projects-voice-kit-magpi-57/)上的[说明，你就可以得到一个谷歌语音交互套件，其中有一堆 IOs 只是尖叫着要好好利用。](https://aiyprojects.withgoogle.com/voice/#assembly-guide)

python 应用程序的源代码[可以从 GitHub 下载，它由一个等待触发的循环组成。这种触发可以是按下按钮或在麦克风附近拍手。当检测到一个触发器时，记录器功能接管发送流到谷歌云。语音到文本的转换在那里进行，结果通过文本到语音引擎返回，帮助系统进行反馈。存储库建议官方语音工具包 SD 镜像(](https://github.com/google/aiyprojects-raspbian) [893 MB 下载](https://dl.google.com/dl/aiyprojects/voice/aiyprojects-latest.img.xz))是基于 Raspbian 的，所以不要马上刷新存储卡，你应该能够将它添加到现有安装中。

如果你还没有获得官方工具包，但只是渴望尝试一下，那么不要再看了。谷歌很友好地发布了一个指南，将谷歌助手支持添加到树莓 Pi 3 中。单板计算机已经有一个扬声器输出，还有大量的 USB 麦克风可以完成这项工作。USB 声卡工作也很好，在你按照说明设置了[谷歌 SDK](https://developers.google.com/assistant/sdk/) 之后，你就有了一个助手。

如果你想完成谷歌 AIY 工具包的体验，你将不得不做一点黑客。添加一个按钮来触发助手脚本是非常简单的，如果有人想添加一个 [DIY 鼓掌触发器](http://hackaday.com/2014/12/09/clap-on-a-breadboard/)来代替，那就去做吧。

 [https://www.youtube.com/embed/7WtSdWSv7uo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7WtSdWSv7uo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 一个自己动手的，可视化的 Alexa

> 原文：<https://hackaday.com/2016/10/17/a-diy-visual-alexa/>

与计算机交谈现在非常流行。我们习惯于用声音相互交流，所以这是有道理的。然而，通过电话线与人交谈和面对面交谈是有明显区别的。与通过电话或无线电交谈相比，你可以亲自获得很多视觉线索。

今天，大多数支持语音的系统就像通过电话连接到计算机。它完成了工作，但你并不总是得到最大的好处。为此，[Youness]决定在他的 Alexa 上安装一个有机发光二极管显示器，为 Alexa 的当前状态提供视觉反馈。这是一项正在进行的工作，但你可以在下面的视频中看到这个想法的两个化身。

树莓皮提供了动力和展示。一个 Python 程序连接到 Alexa 语音服务(AVS)来理解该做什么。AVS 为构建支持语音的应用程序提供了几个接口:

*   语音识别/合成–理解并生成语音。
*   警报–处理计时器或用户话语等事件。
*   audio player–管理音频播放。
*   playback controller–管理播放队列。
*   扬声器-控制音量控制。
*   系统-向 AVS 提供客户信息。

我们已经看到 AVS 被用来创建一个 [Echo 克隆](https://hackaday.com/2016/08/19/retrofitting-a-vintage-intercom-to-run-amazon-alexa/)(不过是在一个复古的例子中)。我们最近还研究了树莓派上的[谷歌语音 API](https://hackaday.com/2016/10/14/raspberry-pi-want-a-cracker/) 。

 [https://www.youtube.com/embed/GFPWN-TU9p8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GFPWN-TU9p8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/pVgv12EAwYA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pVgv12EAwYA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


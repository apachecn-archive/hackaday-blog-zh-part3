# 能读懂你情绪的树莓派机器人

> 原文：<https://hackaday.com/2016/11/17/raspberry-pi-robot-that-reads-your-emotions/>

将机器智能添加到您的黑客中变得越来越容易，甚至有时您不必安装任何特殊软件。在这种情况下，[Dexter Industries]通过使用[谷歌云视觉](https://cloud.google.com/vision/)，为他们的移情机器人增加了[读取人类情感的能力。](http://www.dexterindustries.com/projects/raspberry-pi-robot-that-reads-emotions/)

按下机器人上的一个按钮，它就会向前移动，直到离一个物体有一定的距离。然后，它拍摄一张照片，并将其发送到谷歌云视觉，同时请求进行人脸检测。谷歌返回的响应是 JSON 格式的，如果它找到一张脸，包括这张脸是高兴、悲伤、悲伤还是惊讶的可能性。机器人解析这个响应，并使用文本到语音转换软件给出一个合适的录音语音，例如“你看起来很开心！告诉我你为什么这么开心！”。

[Dexter]已经在 github 上发布了[源代码。它是用 python 写的，即使只有一点编程经验的人也很容易读懂。休息后的视频给出了一些演示，包括一些非人类的主题。](https://github.com/DexterInd/GoPiGo/tree/master/Projects/Empathybot)

在他们的网页上，[德克斯特工业]也给出了进一步的分析。例如，一个受试者有胡须，这给谷歌解释情绪带来了困难。但经过一些修整后，解释得到了改善。不过，对婴儿来说确实有困难，可能是因为胖乎乎的脸颊。

 [https://www.youtube.com/embed/izj8hpqGHy8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/izj8hpqGHy8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们最近看到了其他使用机器智能软件的黑客例子。【德克斯特】在[之前已经使用谷歌云视觉对糖果](http://hackaday.com/2016/10/31/sort-your-candy-with-a-raspberry-pi-and-google-cloud-vision/)进行分拣。在此之前，谷歌的 Tensorflow 被一个机器人[用来识别并说出车库周围物体的名称](https://hackaday.com/2016/10/09/tensorflow-robot-recognizes-objects/)。
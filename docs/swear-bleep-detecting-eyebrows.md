# 脏话哔哔声检测眉毛

> 原文：<https://hackaday.com/2016/11/10/swear-bleep-detecting-eyebrows/>

在广播电视上发誓，他们会发出哔哔声来保护公众的感情。骂人的哔哔声在 1kHz 是相当标准化的，大约是[mechatronicsguy]告诉我们的。你每天都学到新的东西。

好吧，好像没有 ISO 文件详细说明当有人在镜头前说脏话时使用的确切音调，更有可能的是，1kHz 的音调是工作室中最有可能出现的频率。它无处不在，甚至连音调不完美的音频工程师都可以识别它，我们的一个熟人发誓多年接触的一个人给了他的耳朵一个选择性陷波滤波器。

有了这些信息，[mechatronicsguy]创造了一个有趣的项目。作为[electroBOOM] Youtube 频道的粉丝，他为他的易发哔哔声的英雄制作了一套 LED 眉毛，并使用 Teensy 及其音频和 FFT 库[他让它们在检测到 1kHz 音调时点亮](https://tinkerings.org/2016/11/08/swear-detector-with-fft-teensy-electroboom/)。这不是最神奇的方法，但如果你发现自己在寒冷的 11 月早晨需要微笑，那么也许它会对你产生和我们一样的效果。他发布了一个“眉毛在行动”的快速视频，我们把它嵌入到了休息的下面。

 [https://www.youtube.com/embed/QRlCyYPPdTE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QRlCyYPPdTE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果这个有点琐碎的项目激发了你对 Teensy 音频库功能的兴趣，[我们几年前曾更详细地讨论过这个项目](http://hackaday.com/2014/09/30/the-teensy-audio-library/)。
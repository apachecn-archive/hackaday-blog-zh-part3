# 用声卡测量超音速

> 原文：<https://hackaday.com/2017/03/10/supersonic-speed-measurement-with-a-sound-card/>

你可能会想，如果你需要测量一个对于你的高速相机来说太快的抛射体的速度，你将不得不投资一些非常昂贵的设备。

这就是[尼克·摩尔]面临的问题，他得出的解决方案极其简洁优雅。他在抛射体的路径上安排了一对箔带，当抛射体穿过箔带时，箔带断裂，他测量了断裂之间的时间。聪明之处不在于录像带，而在于他如何衡量时机。他不再依赖堆满设备的实验室，而是使用他的计算机声卡。输出通过每盘磁带向输入发送一个音调，使用 Audacity，他可以捕捉两个音调，并测量左右声道中每个音调结束之间的时间。

在休息时间下面的视频中，他演示了以每秒 496.5 米的速度测量超音速粒子的速度，对于这样一个相对简单的设备来说，这是一个相当大的成就。他当然可以通过提高采样频率来提高分辨率，但我们猜测选择 48 kHz 很大程度上是因为他的声卡质量。然而，用这样一个相对基本的设备实现这一点是一个整洁的成就。

 [https://www.youtube.com/embed/Pl9F81kCKaM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Pl9F81kCKaM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这个项目并不是我们向你展示的测量高速射弹的唯一尝试，还有这个高速 [Nerf 飞镖速度计](http://hackaday.com/2014/08/03/supersonic-nerf-dart-speedometer/)。我们已经将这一领域进一步带入科学领域，[测量声速](http://hackaday.com/2012/08/27/measuring-the-speed-of-sound-with-science-and-statistics/)。

谢谢[马修·西蒙斯]的提示。
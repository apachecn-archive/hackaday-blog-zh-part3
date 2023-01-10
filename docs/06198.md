# 小偷小心:一个私家侦探看着

> 原文：<https://hackaday.com/2017/07/13/sneak-thieves-beware-a-pi-watcheth/>

有没有那种奇怪的感觉，有人闯入你的工作间？好吧，Hackaday.io 用户[Kenny]制作了一个教程，教你如何通过把你可能有的备用树莓皮变成一个安全摄像头系统来挠痒痒，该系统会在瞬间通知你。

该系统是这样工作的:一个 Raspberry Pi 3 和连接的摄像头模块保持警惕，不断扫描运动并记录视频。如果检测到运动，它会立即抓拍并通过 PushBullet 向用户的手机发送图片，然后开始录制视频。如果几秒钟后仍有运动，则重复该过程，直到该区域再次没有运动。这也允许与您的 Pi 安全系统进行双向通信，因此您可以随时查看实时提要。

假设您的 Pi 最近已经更新，为了让它为您工作，设置需要设置一个 PushBullet 帐户，并将其安装在您的手机上，并与 API 链接。对于您的 Pi，您可以继续设置一些 Python 推组件库，安装 FFmpeg、Pi 相机通知程序等等。或者，安装【Kenny】已经[准备好](https://iotbreaks.com/build-a-camera-alert-application-with-raspberrypi-3-and-iosandroid-pushbullet-app/)的现成镜像。他在他的指南中深入探讨了代码的本质，所以休息后可以去看看或者观看教程视频。

 [https://www.youtube.com/embed/iwZf02XtVnQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iwZf02XtVnQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



你也可以用一个 [Pi Zero](http://hackaday.com/2017/03/26/turn-that-pi-zero-into-a-streaming-camera-step-by-step/) 来缩小这个过程，甚至把你的窥视孔变成一只[永远监视的眼睛](http://hackaday.com/2013/09/17/stealth-peephole-camera-watches-your-front-door/)。
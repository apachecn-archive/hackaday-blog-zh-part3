# 用树莓派和谷歌云视觉给你的糖果分类

> 原文：<https://hackaday.com/2016/10/31/sort-your-candy-with-a-raspberry-pi-and-google-cloud-vision/>

如果你离开了“不给糖就捣蛋”的游戏，带着一堆糖果回家，你到底能做些什么来处理这个问题并按品牌分类呢？

是的，这是我们很多人在每年的这个时候都不得不面对的问题。挑战如此之大，以至于[Dexter Industries]的人已经制造了一个机器人糖果分拣机来自动完成这项任务。

好吧，这个应用程序有点半开玩笑的味道。但是他们使用的技术很有趣，值得再看一眼。硬件方面，它是一个乐高 Mindstorms 输送机和料斗，通过 BrickPi 界面由树莓 Pi 控制。一切都很好，但是兴趣在于软件。他们用 Raspberry Pi 的摄像头拍摄照片，然后发送到 Google Cloud Vision，然后进行查询，返回对有问题的糖果品牌的猜测。然后将返回的值与品牌列表进行比较，以保留或捐赠给另一个家庭成员，漏斗将酒吧倒入相应的堆中。他们提供了完整的构建细节和代码，以及我们放在休息下面的视频。简单到一个孩子都能解释。

 [https://www.youtube.com/embed/B61xx4DGUwo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B61xx4DGUwo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



机器视觉仍然是一个挑战，正如我们从[我们的故事列表中看到的那样，标签是](http://hackaday.com/tag/machine-vision/)；这些年来只有少数几个 Hackaday 存在过。使用云服务可能不符合每个人的口味，但它提供了进入机器视觉的替代途径以及谷歌引擎的额外功能，并可能向可能不会使用该技术的制造商开放该技术。

[via [Recantha](http://www.recantha.co.uk/blog/?p=15749)
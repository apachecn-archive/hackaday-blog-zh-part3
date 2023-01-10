# 二维步进电机

> 原文：<https://hackaday.com/2018/01/08/a-stepper-motor-for-two-dimensions/>

我们都听说过线性马达，比如推动磁悬浮列车的线性马达，被描述为常规电动马达的“展开”版本。这个类比很恰当，有助于理解线性电机的工作原理，但它回避了一个问题:如果我们可以在两个维度上展开定子，而不是一个维度，会怎么样？

这就是[BetaChecker 的] [双轴步进电机](https://hackaday.io/project/29190-area-stepper-motor-with-wireless-energy-supply)背后的想法，看起来它在一些有趣的应用中有很大的潜力。构建细节很少，但根据我们从视频和 Hackaday.io 帖子中收集的信息，[BetaChecker]创建了一个由 288 个手绕铜线圈组成的压板，每个线圈都可以通过大量 L293 H 桥芯片和 Arduino Mega 进行选择性控制。各种底座中带有钕磁铁的滑板可以应用到压板上，根据线圈的通电方式，滑板可以在任一方向上移动。对于垂直应用，看起来有些线圈用于将滑板固定在压板上，而其他线圈用于推动滑板。每个线圈的孔内都有 RGB LEDs，尽管它们在 zazzle 之外的功能尚不清楚。

我们喜欢更多的细节来衡量它的发展方向，但是有了更好的分辨率，像这样的东西可以成为一个伟大的 3D 打印机床。不过，如果一维运动对你来说足够了，看看这个线性步进电机吧，它的工作原理与此类似。

 [https://www.youtube.com/embed/kjkw7rKhPfc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kjkw7rKhPfc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


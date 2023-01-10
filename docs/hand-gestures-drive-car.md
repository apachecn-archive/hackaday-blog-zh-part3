# 手势驾驶汽车

> 原文：<https://hackaday.com/2016/04/05/hand-gestures-drive-car/>

有许多方法可以不用踏板，有时甚至不用方向盘来控制汽车。最常见的是，这些替代控制机制安装在车主因某种原因残疾的车辆上，但[Anurag]将这种替代控制的想法推进了一步。他制造了一辆仅用手势就能驾驶的汽车。

在一辆遥控汽车上，安装了一个 Raspberry Pi 2 来处理处理和通信。Pi 上创建了一个无线网络，一台笔记本电脑通过网络连接到 Pi。笔记本电脑上的网络摄像头定期以 15 fps 的速度捕捉帧，以检查司机的手势。将图像转换为灰度，阈值化，获得轮廓，并获得质心和最远点。

在完成一些计算之后，做出移动决定。这个决定被传递给 Pi，Pi 又将这个决定传递给汽车的内部芯片。所有代码都可以在[项目的 github 页面](https://github.com/anuragmishracse/HandGesture-CarMovement)上找到。[Anurag]希望这可以在未来扩大到全尺寸汽车。我们之前已经见过依赖声纳传感器的[基于手势的遥控器](http://hackaday.com/2015/12/13/arm-based-gesture-remote-control/)，所以看到一个严格依赖图像处理的遥控器很有趣。

 [https://www.youtube.com/embed/Ez7dM8TuFZA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ez7dM8TuFZA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


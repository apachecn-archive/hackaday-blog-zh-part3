# 通过 3G 的机器人汽车

> 原文：<https://hackaday.com/2016/02/07/robo-car-via-3g/>

[Emil kalst]有一辆[相当结实的遥控车](https://www.youtube.com/watch?v=aa6yq3KtXdc)。我们指的不是一辆你可以在附近开着的手持遥控器的小车。[埃米尔的]汽车有一个摄像头和一部手机，因此它可以去任何有 3G 或 4G 网络的地方。

视频(见下文)展示了结果(以及[埃米尔的]弟弟充当安全员)。如果你想复制一辆类似的车，这段视频提供的诱人细节可能会对你有用。然而，它没有提供完整的细节。

车上的两个电池将为车辆提供超过 20 小时的连续使用。30W 的马达用链传动减速，以达到“行走速度”有一个带有华为 3G USB 加密狗的树莓 Pi，而[Emil]在他温暖的客厅里使用 XBox 控制器来控制方向。当然，Pi 不能直接处理这样的大电机，所以 Phidgets USB 电机控制器完成了这项艰巨的工作。软件是用 Node.js 写的。

摄像机支架可以在伺服系统上旋转 230 度，以便操作员可以扫描前方的道路。视频提到，驾驶汽车需要一个重型伺服金属齿轮(早期的尼龙齿轮尝试没有成功)。

总的来说，它看起来像一个坚实的构建。我们希望[埃米尔]将很快分享代码和更多的细节。如果你等不及了(而且你的保险已经付清)，你可能会试着开一辆更大的车。令人惊讶的是，[不止一个这种](http://hackaday.com/2009/11/10/remotely-control-your-crappy-car-dangerously/)的例子。

 [https://www.youtube.com/embed/aa6yq3KtXdc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aa6yq3KtXdc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


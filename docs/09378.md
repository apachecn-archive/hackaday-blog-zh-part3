# 劳拉系统从远处指挥无人机

> 原文：<https://hackaday.com/2018/05/05/lora-system-commands-drones-from-a-distance/>

在过去的几年里，LoRa 在黑客圈里引起了不小的轰动，因为它提供了一种长距离、低功耗和低成本的迷人组合。它通过在未经许可的频段上使用扩频技术来实现这一点，这意味着它可以将数据发送到令人惊讶的距离，而且你不需要无线电许可证就可以使用它。它主要用于物联网，但[帕韦日·斯彼哈尔斯基]有其他想法:他正在[建立一个系统，用它来控制 5 公里或更远距离的四轴飞行器无人机](https://github.com/DzikuVx/QuadMeUp_Crossbow)。这是一个雄心勃勃的目标，考虑到他正在使用的零件只值几美元。

他正在使用一个[非品牌的 Adafruit Feather](https://www.adafruit.com/product/3079) LoRa 板和几个自制的天线，以及他自己的软件，该软件从 RC 控制器的 Taranis 控制端口获取数据，对其进行编码，并通过 LoRa 无线电发出啁啾声。在另一端，一个类似的无线电接收并解码数据，将其传送给无人机。

这肯定仍是一项正在进行的工作，但他已经让它工作了，让他的无人机在链路上飞行，保持对数百米外的控制。目前，他不能走得更远，因为他的 LoRa 无线电似乎被无人机上的视频链接淹没了，但他正在努力改变频率扩展和跳跃，并使用更好的天线来提供更远的范围。我们之前已经看到过一些来自[Pawel]的有趣的东西，比如他的 [DIY 遥测系统](https://hackaday.com/2016/06/18/easy-diy-telemetry-goes-the-distance/)，所以如果你是无人机爱好者，这个项目值得关注。

 [https://www.youtube.com/embed/Q1DytEuOXJs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Q1DytEuOXJs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/XDg5PgWrrj4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XDg5PgWrrj4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


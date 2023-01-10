# 工业控制器上的 Pong

> 原文：<https://hackaday.com/2016/04/01/pong-on-industrial-controllers/>

可编程逻辑控制器(PLC)是控制自动化的主要部分。在 60 年代或 70 年代的某个时候，他们替换了一个装满继电器的盒子，以实现那种“如果-这个-那么-那个”的逻辑，打开恒温器或指挥机器。在 90 年代或 2000 年代的某个时候，增加了一些计算能力，给了我们可编程自动化控制器(PAC)。如果阅读 Hackaday 教会了我们什么，那就是如果你给人们一点点计算能力，他们就会实现 Pong(或 Snake 或 Doom！).

我们收到了一个链接，[绝对自动化]就是这么做的:[在一点工业控制上实现了一个可远程播放的 Pong](http://www.absolutelyautomation.com/articles/2016/03/22/video-game-pac-using-rfb)。即使你身边没有政治行动委员会，细节也很有趣。

第一步是把图形拿出来。有问题的 PAC 已经能够说以太网，所以“只是”发送正确的数据包的问题。也许最简单的方法是实现 VNC 的远程帧缓冲(RFB)协议，然后在 PC 上使用 VNC 客户端发送图形。(正如他们指出的，[CNLohr]在 ESP8266 (YouTube) 上也做得很好。)于是就有了 RFB 图书馆。[AbsolutelyAutomation]指出，这可以用来制作一些无聊的东西，比如用户友好的配置和监控屏幕。(哈欠！)

图形完成后，很容易在顶部添加一个 Pong 层，使用基于流程图的编程接口，向 PLC/PAC 作为工业控制器的常用功能致敬。(奇怪的是，它似乎要编译成第四种方言才能在 PAC 上运行。)然后你就在玩。如果你想了解更多信息，这里有[代码](http://www.absolutelyautomation.com/sites/default/files/160322_OPTO22_GAME_RFB.zip)和 [(PDF)文章](http://www.absolutelyautomation.com/sites/default/files/160322_VIDEO_GAME_IN_PAC_USING_RFB.pdf)。如果你没有运行它的 PAC，[制造商为你准备了一个模拟器](http://www.opto22.com/site/downloads/dl_drilldown.aspx?aid=3690)。

我们从未与 PLC/PAC 合作过，但当我们看到它时，我们知道黑客精神。在我们的书里，让通常放在锅炉房的东西玩电子游戏是最棒的。这让我想起了几年前在 DEF CON 上的一个工业控制黑客室。也许这就是今年在那个场地花些时间所需要的灵感。

我们知道我们有控制工程师。你编进 PLC 的最奇怪的东西是什么？
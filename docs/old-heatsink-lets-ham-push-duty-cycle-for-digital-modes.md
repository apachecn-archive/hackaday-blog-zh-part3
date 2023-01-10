# 旧散热器让汉姆推动数字模式的占空比

> 原文：<https://hackaday.com/2016/11/22/old-heatsink-lets-ham-push-duty-cycle-for-digital-modes/>

听业余无线电乐队足够长的时间，你可能会得出结论，火腿永远不会停止说话。当然，这只是表面现象，以一种语音模式工作的发射机的占空比可能非常低。但是数字模式可以增加占空比，并真正给钻机上的决赛带来压力，所以[这种适合现场的火腿收发器散热器](https://www.youtube.com/watch?v=zqtH8i7HtP0)是一个需要记住的方便技巧。

这个黑客来自于[Kevin Loughin (KB9RLW)]，他正在尝试使用他的“盒子里的小屋” [Yaesu FT-817](https://en.wikipedia.org/wiki/Yaesu_FT-817) 进行 PSK31 之类的数字模式。数字模式本质上是将收发器变成一个低波特调制解调器，因此信息可能需要很长时间才能发送。这给 5 瓦的 FT-817 带来了一个问题，它是为便携式操作而设计的，没有大型基站钻机所具有的冷却风扇和沉重的散热器。[Kevin]发现，一个旧的 486 CPU 散热器夹在后面板上的一个凸耳上，增加了足够的热质量，以保持决赛冷得多，即使在收音机的全 5 瓦输出下有 4 分钟的死键进入假负载。

您可能会嘲笑这种解决方案的简单性，我们不得不承认这远不是一个史诗般的黑客。但是有时候记住简单的修正是值得的。然而，如果你的项目需要少一点凭直觉，多一点工程学，一定要看看[Bil Herd]关于热管理的[初级读本](http://hackaday.com/2014/03/03/hot-or-not-find-out-how-to-calculate-component-heat-and-why-you-should/)。


 [https://www.youtube.com/embed/zqtH8i7HtP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zqtH8i7HtP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[无线电/业余无线电](https://www.reddit.com/r/amateurradio/comments/5dgmgw/cooling_the_yaesu_ft817_for_digital_modes/)
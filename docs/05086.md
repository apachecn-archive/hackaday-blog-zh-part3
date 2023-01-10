# T-Rex Runner 在晶体管测试仪上运行

> 原文：<https://hackaday.com/2017/02/22/t-rex-runner-runs-on-transistor-tester/>

如果你曾经花时间在网上购买电子产品——这意味着我们几乎所有人——那么网站迟早会听到你的购买狂潮，并开始提供购买更多无用物品的“建议”广告。一种通常提供的流行产品似乎是通用元件测试仪，通常称为“Mega328 晶体管测试仪二极管三极管电容 ESR 计”。这些包括一个 ATmega328，一个 SPI 液晶显示器，一个按钮，一个 ZIF 插座和一些其他组件。几乎所有这些都是由[Markus Frejek]开发的出色的 AVR 晶体管测试仪项目的廉价复制品。[Robson Couto]得到了其中一个克隆组件测试器，玩了一会儿后，决定黑掉它，为它写一个 [T-Rex runner 游戏](http://dragaosemchama.com/2017/01/rex/)。

T-Rex runner 游戏是 Chrome 为你提供的在无法连接互联网时消磨时间的游戏。它只需要一个按钮就可以玩。这只是一种简单的游戏，可以很容易地移植到组件测试人员。从[Robson]的博客文章中可以看出，他并没有为连接到 LCD 显示器的 ATmega 编写一个简单的游戏，而是详细介绍了这个过程，这对于其他想尝试编写游戏的人来说很有用。

经过一些在线调查和一些万用表测试，他能够找出 LCD 控制器芯片连接到 ATmega 的 D 端口，这意味着通过位碰撞使用软件 SPI。然后，他查看被拆卸的固件内部，寻找对端口 D 的写入，以找出引脚分配。当然，在完成所有这些工作后不久，他发现了一个带有 pin 映射的 config.h 文件。

有了这些信息，他就能够使用 Adafruit ST7565 库来驱动 LCD，但不是在翻转图像之前。他的 ST7565 库的[修改版 fork 在 GitHub 上有。他的](https://github.com/robsoncouto/ST7565-T3)[游戏代码](https://github.com/robsoncouto/rex)也是可用的，但是阅读整个开发过程是非常有趣的。休息之后，请观看跑步比赛的视频。

在之前的一篇帖子中，我们对这些廉价的[晶体管测试器](http://hackaday.com/2015/04/24/review-transistor-tester/)进行了产品评测，如果你有一台这样的测试器，给[罗布森]的游戏一个旋转——在你等待回流焊炉完成焊接周期时，它会很方便。

 [https://www.youtube.com/embed/PiM1qX1G1Is?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PiM1qX1G1Is?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


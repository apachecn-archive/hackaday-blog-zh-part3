# 微型游戏机是一个微型手持游戏机

> 原文：<https://hackaday.com/2018/02/27/microgamer-is-a-microbit-handheld-console/>

针对教育的 BBC micro:bit 单板 ARM 计算机并不像其竞争对手那样经常出现在这些页面中。这不是最便宜的板，除了最基本的方式外，其他所有方式的接口都需要一个稍微深奥的边缘连接器。然后，我们非常高兴地看到，edge connector 由[杨奇煜·乔托]用他的掌上游戏机[变成了一项功能，他使用 micro:bits 对不同的游戏进行预编程，就像商用游戏机中的游戏盒一样。](https://hackaday.io/project/47760-microgamer)

micro:bit 位于一对 AAA 电池上方的手持 PCB 底部的 edge 连接器中，而另一侧是有机发光二极管显示器和常用的一组按钮。这是一个特别简单的板，因为 micro:bit 包含支持其外设所需的所有电路。

他使用 Arduino IDE 和 Arduboy2 库的修改版本编写游戏代码，这使得他可以轻松移植为 Arduino 硬件编写的 Arduboy 游戏。这是一项正在进行的工作，因为还有更多的功能要加入，但使用 micro:bits 作为墨盒的想法是相当特殊的。有一个视频的控制台在行动中，我们把它放在下面的休息。

 [https://www.youtube.com/embed/HiNHSsFAe5o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HiNHSsFAe5o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果 micro:bit 激起了你的兴趣，你可能想看一看[它的软件栈](https://hackaday.com/2017/12/02/exploring-the-bbc-microbit-software-stack/)，并看看[我们的评论](https://hackaday.com/2016/06/03/hands-on-with-the-bbc-microbit/)。
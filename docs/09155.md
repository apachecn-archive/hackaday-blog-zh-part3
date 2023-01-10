# 大嘴巴比利巴斯频道麦莉赛勒斯

> 原文：<https://hackaday.com/2018/04/14/big-mouth-billy-bass-channels-miley-cyrus/>

多亏了 Alexa ，这位大嘴巴比利·巴斯有了额外的嘴唇。如果你还不熟悉的话，大嘴比利巴斯是一种非常受欢迎的会唱歌的电子鱼，它被设计成一种挂在墙上的奖杯鱼。在库存状态下，每当有人走过时，Billy 就会用一个运动传感器开始唱歌。它只限于几首歌，除非你喜欢黑东西——在这种情况下，它是一堆包裹在一条幽默的鱼里的可用部分！Hackaday 自己的[Bob Baddeley]将鱼与亚马逊 Echo Dot 结合起来，用 ATtiny84 将二者连接起来，并让 Billy 为 Alexa 代言。

[Bob]有一些问题需要解决，包括在播放音频时让 Billy 的嘴动起来，检测回声何时打开，移动马达并播放音频。经过一点研究和大量的调整，一个为 ATtiny 设计的快速傅立叶变换算法被用来让嘴动起来。由于鱼的设计，嘴没有动很多，而且[鲍勃]对它进行了一点修改，但他能做的也就这么多了。

鱼躺在那里唱歌当然很好，但[鲍勃]想让比利在 Alexa 听的时候动一动，为了检测到这一点，最好的办法是观察这个点的灯是否亮了。他尝试了几种方法，但认为最简单的方法可能是最好的，最终只是在 LED 上贴一个光敏电阻。现在，当你问 Alexa 问题时，Billy 会转头看着你。

对 Dot 的外壳进行了一些修改，现在一切都适合原来的安装板，在钻了一些孔以便 Dot 可以听到后，工作了。比利已经从只有几首歌变成了一个庞大的歌曲库。

我们以前见过 Alexa 和大嘴巴 Billy Bass 的组合，但只是演示，从来没有像 Bob 这样优秀的向导。这个指南的好处在于，一旦你黑了硬件，使用 Alexa 技能添加新功能[就轻而易举了。](https://hackaday.com/2018/01/17/an-alexa-skill-among-other-things-in-a-few-minutes/)

 [https://www.youtube.com/embed/ZiV7wmwY7sY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZiV7wmwY7sY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


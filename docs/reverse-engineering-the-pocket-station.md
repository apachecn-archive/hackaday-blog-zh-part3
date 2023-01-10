# 索尼 PocketStation 的逆向工程

> 原文：<https://hackaday.com/2016/10/05/reverse-engineering-the-pocket-station/>

[罗布森·库托]年轻时从未真正拥有过 PlayStation 游戏机，但这并不意味着他在以后的生活中不能复兴。尤其是一款名为[pocket station 的日本专属配件引起了他的兴趣](http://dragaosemchama.com/2016/09/backup-e-gravacao-de-memory-card-ps1/)。

这个有问题的东西位于 PlayStation 的存储卡插槽中。它的目的是给游戏增加额外的功能，并有希望推销自己。比如 PokeWalker，Kinect 等。这是一个古老的策略，但是这个袖珍站有一些有趣的事情发生。

最大的是它的处理器。尽管它有一个可怜的 32×32 单色屏幕，但它与 GameBoy Advance 采用了相同的处理器。从一家互联网拍卖行获得一张卡后，[Robson]想为这款设备加载一些 rom，看看它是什么样的。

这需要相当多的工作。幸运的是，由于仿真场景，有大量的文档在互联网上流传，没过多久，他就说服了一个微控制器假装成存储卡插槽。现在，任何有一些技能和一点游戏历史的人都可以在 PocketStation 上玩罕见的 ROM 转储。
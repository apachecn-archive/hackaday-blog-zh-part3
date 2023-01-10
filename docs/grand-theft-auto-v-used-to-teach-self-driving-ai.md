# 侠盗猎车手 V 用来教自动驾驶 AI

> 原文：<https://hackaday.com/2016/09/16/grand-theft-auto-v-used-to-teach-self-driving-ai/>

尽管驾驶过程非常复杂，但对行人、环境条件、甚至道路的基本规则做出反应已经成为人们的第二天性。就人工智能而言，当现实世界充满了黏糊糊的人类和其他潜在的灾难时，教机器学习算法如何在虚拟世界中驾驶是有意义的。那么，为什么不使用大获成功的《侠盗猎车手 V》虚拟世界[来教机器学习程序驾驶车辆](http://download.visinf.tu-darmstadt.de/data/from_games/)？

这种方法的难题是获得足够大的样本，使机器学习可行。想法是这样的:与从现实世界图像中注释对象数据的耗时任务相比，虚拟世界提供了一种更有效的解决方案来为这些程序提供足够的数据。除了扩大数据量，研究人员还可以操纵天气、交通、行人等来创造复杂的条件来训练人工智能。

教“交通规则”很容易——我们一直在教 16 岁的孩子。但那些最早的司机，已经花了一辈子的时间观察现实世界，看父母开车。GTA V 内部的虚拟世界非常逼真。人类是伟大的模式识别者，善变的游戏玩家会对任何不模拟现实生活的事情大喊犯规。我们剩下的是一个近乎完美的测试案例来源，用于机器学习，以应用于自动驾驶的艰难部分:理解每辆车遇到的巨大变化的世界。

来自英特尔实验室和德国达姆施塔特大学的一组研究人员创建了一个自动索引虚拟世界的程序(如上所示)，为机器学习程序创建有用的数据以供消费。请注意，这并不能完全取代现实世界的经验，但在将人工智能放在车辆后面之前犯一些错误的自由有可能加快自动驾驶汽车的发展。阅读该团队发表的论文 [*为数据而玩:来自视频游戏*](http://download.visinf.tu-darmstadt.de/data/from_games/data/eccv-2016-richter-playing_for_data.pdf) 的真相。

 [https://www.youtube.com/embed/JGAIfWG2MQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JGAIfWG2MQQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在你认为这可能会变得非常糟糕之前，看看这辆[迷你拉力卡车，它教会了自己如何电动滑行](http://hackaday.com/2016/05/29/autonomous-truck-teaches-itself-to-powerslide/)，并意识到这种教人工智能如何驾驶的方法实际上可能非常棒。还要意识到，这项研究只是描述了每幅图像 7 秒钟的静止图像。这比真实世界的图像快了几个数量级——这对学习来说很好，但我们离实时和真实世界的实现仍然很远。

我们真的希望一个研究助理团队在严肃的科学工作中扮演大量的 GTA V 来收集这个数据集。这让我想起了一个严重的减速带。这款游戏是受版权保护的，你不能对游戏的录像做任何你想做的事情，研究人员确实提到，在某些非商业环境下，游戏镜头是允许的。这意味着，优步、谷歌、苹果、特斯拉、每一家主要的汽车公司，以及任何其他将自动驾驶汽车作为商业模式开发的人，都将被排除在这个数据源之外，除非 Rockstar Games 提出一个许可模式。也许你的下一辆车会贴上“由 GTA 提供动力”的标签。

[ [麻省理工科技评论](https://www.technologyreview.com/s/602317/self-driving-cars-can-learn-a-lot-by-playing-grand-theft-auto/)经由[科普](http://www.popsci.com/)
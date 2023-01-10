# 在康威的生命游戏中构建一个俄罗斯方块的工作游戏

> 原文：<https://hackaday.com/2017/09/17/building-a-working-game-of-tetris-in-conways-game-of-life/>

如果你没有跟随康威的生活游戏，它已经从 1970 年发表在《科学美国人》上的数学难题走了很长的路。多年来，数学家们已经发现了一系列符合生命规则的构造，包括许多可以用来执行编程功能的构造——逻辑门、锁存器、多路复用器等等。这些创造中的一些已经变得相当巨大和复杂，至少就生命细胞而言。例如，OTCA 元像素由 64，691 个细胞组成，能够模仿生活中发现的任何细胞自动机。

一群黑客利用 OTCA 超像素技术从生命元素中创造了一款[俄罗斯方块游戏。该游戏的特点是所有 7 种形状，以及人们所期望的移动、旋转和下落。你甚至可以预览下一首曲子。这个游戏是许多人的作品，他们在这个更大的程序的各个部分工作。他们用《生活游戏》的元素建造了一台 RISC 计算机，以及它的汇编器和编译器，由](https://codegolf.stackexchange.com/questions/11880/build-a-working-game-of-tetris-in-conways-game-of-life)[的 OTCA 超像素](http://www.conwaylife.com/wiki/OTCA_metapixel)来承担重任。(帖子顶部的图片是程序的数据同步器。

在 GitHub 上查看[项目的源代码](https://github.com/QuestForTetris)，使用[这个解释器](http://play.starmaninnovations.com/qftasm/)。将内存设置为 3-32，然后点击运行。

对于生命创造的其他几个例子，请查看我们之前发布的生命时钟的[游戏和由生命自动机](https://hackaday.com/2017/03/11/a-clock-created-with-conways-life/)合成的[音乐。](https://hackaday.com/2011/03/27/music-synthesized-from-the-game-of-life/)
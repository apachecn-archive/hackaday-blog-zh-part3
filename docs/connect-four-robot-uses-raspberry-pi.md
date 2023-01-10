# 用树莓派连接四个机器人

> 原文：<https://hackaday.com/2016/03/03/connect-four-robot-uses-raspberry-pi/>

大多数人玩游戏是为了娱乐。黑客制造机器人来玩游戏娱乐。这就是[pland chips]所做的。他用一个树莓派和一套工具组装了一个四人游戏机器人。这个名为 4-Bot 的机器人必须做两件事:第一，它必须能够操纵棋子。其次，它必须能够看到棋盘。MeArm 赋予 4-Bot 操纵能力，一个聪明的扫描系统完成了这个任务。

建造一个游戏机器人还有另外一个组成部分:大脑告诉它如何玩一场胜利的游戏。4-Bot 使用 Python 来实现众所周知的 minimax 策略。即使是一个 6×7 的棋盘，也有超过 4 万亿个可能的游戏位置，所以你需要一个智能算法来在合理的时间内玩好。你可以在下面的视频中观看机器人比赛。

我们之前已经看过很多次游戏机器人了。有些人甚至[玩电脑游戏](http://hackaday.com/2014/04/17/lego-robot-plays-games-for-you-as-you-sleep/)。如果你需要一个手臂，你可以[在 Hackaday 商店](http://store.hackaday.com/products/mearm-pocket-sized-robot-arm)买一个，或者自己做一个——这些都是开源的，并且设计成易于激光切割。

 [https://www.youtube.com/embed/rbFIqerYCKc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rbFIqerYCKc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


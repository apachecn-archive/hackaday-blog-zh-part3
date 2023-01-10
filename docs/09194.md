# 和鬼魂下棋

> 原文：<https://hackaday.com/2018/04/19/play-chess-against-a-ghost/>

虽然国际象棋长期以来一直是人类优于计算机的领域，但天平已经明显向有利于计算机的方向倾斜。但是人类仍然可以控制的是碎片本身。也就是说，直到现在。一个小组制造了一个机器人，它既使用了一个具有挑战性的象棋引擎，又能移动自己的棋子。

来自创造者[Tim]、[Alex S]和[Alex A]的机器人能够使用桌子下的机械臂和电磁铁操纵游戏板上的棋子。它由一个 Raspberry Pi 控制，该 API 还运行一个 Stockfish 象棋引擎实例来玩象棋游戏。一个明显的障碍是如何防止机器人将棋子相互碰撞，这可以通过在一个大棋盘上使用小棋子，并总是在方格的边缘移动棋子来解决。

这是一个非常有趣的项目，尤其是考虑到它是用很少的预算建造的。而且，如果你不熟悉 Stockfish，它是最强大的象棋引擎之一，而且碰巧是免费和开源的。在之前，我们已经看到它[被用在其他一些棋盘上，尽管那些棋盘不能移动自己的棋子。](https://hackaday.com/2016/07/08/digital-opponent-in-an-analog-package/)

 [https://www.youtube.com/embed/5MZTQNxuwCw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5MZTQNxuwCw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


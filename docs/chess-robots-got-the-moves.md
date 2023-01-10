# 象棋机器人会走了

> 原文：<https://hackaday.com/2017/09/26/chess-robots-got-the-moves/>

[RoboAvatar]的[象棋机器人](https://www.instructables.com/id/Homemade-Chess-Robot/)由一个安装在龙门架上的手臂组成，它根据软件的指示拾取棋子并将它们放置在新的位置。当玩白棋的人走一步时，游戏开始。当一局游戏结束后，人类玩家按下一个按钮，让机器人开始游戏。你可以在我们发布在休息时间下方的视频中看到它的作用。

运行机器人的是一个 Arduino UNO，带有一个 MUX shield 和一对 MCP23017 I/O 扩展器芯片，总共有 93 个引脚可用！由于所有这些引脚，Arduino 能够监听 64 个簧片开关，每个方块一个。

机器人通过听簧片开关来检测人类的动作，并识别何时有变化。该机架由 PVC 板制成的 X 和 Y 轨道组成，带有由 NEMA-23s 转动的半英寸丝杠，由 ST-6600 步进驱动器供电。

与一些依赖现有软件的象棋机器人不同，这款机器人采用了定制的 minimax 象棋算法，由[RoboAvatar]自己编码。它由运行在计算机上的 Python 脚本组成，通过串行连接与 Arduino 交互。在第二个视频中，他解释了他的算法是如何工作的。你也可以从[RoboAvatar]的 [GitHub 库](https://github.com/RoboAvatar65/ChessRobot)下载 Arduino 和 Python 文件。

你会惊讶我们已经发布了多少下棋机器人，像 [ChessM8](https://hackaday.com/2015/03/15/lonely-build-yourself-a-chess-robot/) 机器人和这个[声控象棋机器人](https://hackaday.com/2013/05/09/voice-controlled-chess-robot/)。

 [https://www.youtube.com/embed/NefiXZ7BCsE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NefiXZ7BCsE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/PHNAgpt3Pj0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PHNAgpt3Pj0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


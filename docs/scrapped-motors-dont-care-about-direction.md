# 报废的电机不在乎方向

> 原文：<https://hackaday.com/2018/05/19/scrapped-motors-dont-care-about-direction/>

轮盘赌或桌面棋盘游戏等机会游戏中内置的旋转器在被给予良好的旋转后会在一个随机数字上停止。没有诀窍，但他们最终会因为摩擦而休息，不管你的兄弟姐妹为赢得比赛有多努力。如果旋转永远持续下去，并且因为没有控制器而没有编程，那会怎么样？[Ludic Science]向我们展示了他用一个废弃的硬盘驱动马达和一个变压器制作一个永久旋转器的方法。他的视频也可以在休息下面看到。

公平的警告:这涉及到主电源。硬盘驱动器中的无刷电机依赖于不同频率的三相电流，但来自单个变压器的功率将是 50 或 60Hz 的单相交流电。这大大简化了事情，但我们失去了电机和方向控制的自启动能力，但我们在我们的永久旋转器中调用这些功能。由于缺相，我们的无刷电机无论朝哪个方向启动都会蹒跚而行，但电路再简单不过了。

这只是一个报废硬盘电机简历上的最新技能。他们将使用 9V 电池运行[，或者逆向运行](http://hackaday.com/2016/09/21/brushless-hdd-motor-driver-from-9v-and-painters-tape/)[成为编码器](http://hackaday.com/2018/01/07/scrap-a-hard-drive-build-a-rotary-encoder/)。如果你想使用它更像制造商的意图，[考虑这个控制器](http://hackaday.com/2016/07/29/3-phase-bldc-motor-controller-will-run-you-20-in-parts/)。

 [https://www.youtube.com/embed/ycb6waem0HU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ycb6waem0HU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[Itay]。
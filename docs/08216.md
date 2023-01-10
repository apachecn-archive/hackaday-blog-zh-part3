# 数字捕鼠器

> 原文：<https://hackaday.com/2018/01/11/digital-mouse-trap/>

许多电脑游戏依赖鼠标输入，浏览器游戏也不例外。然而不幸的是，这并不总是最直观的控制器。[Nathan Ramanathan]联合了几个黑客，得到了他想要的控制器，可以玩像 Agar 和 Slither 这样的浏览器游戏。在这个项目中没有啮齿动物受到伤害。

他想主导的游戏是自上而下的视图，所以没有必要将鼠标移动到远离屏幕中心的地方。为了更直观的界面，选择了带有集成操纵杆的 Wii 双截棍。双截棍是[出了名的](https://hackaday.com/2013/12/14/wii-nunchuck-controlled-tetris-on-a-raspberry-pi/) [可砍的](https://hackaday.com/2012/09/25/wii-nunchuck-controlled-robot-exhibits-rock-solid-balancing/)。一个 Arduino 将双截棍的数据转换成鼠标的移动。在电脑内部，Autohotkey 将鼠标指针控制在有用的位置。Autohotkey 是一个用于执行键盘和鼠标宏的脚本工具。

结果是一个操纵杆控制这些浏览器游戏，就像你期望操纵杆控制游戏一样。鼠标功能，包括标准和快速滚动，是一个额外的奖励，所以像《我的世界》这样的游戏不会落后。双截棍的人体工程学让我们想知道为什么它没有出现在更多可穿戴的黑客中。

定制游戏控制器对黑客读者来说并不陌生。我们见过他们用[乐高积木](https://hackaday.com/2014/07/30/a-lego-game-controller-just-for-the-hack-of-it/)、[汽车](https://hackaday.com/2017/12/30/34c3-using-your-car-as-video-game-controller/)，甚至[装饰地毯](https://hackaday.com/2016/11/29/game-controller-cuts-the-rug/)搭建而成。

 [https://www.youtube.com/embed/gBDbNetSw2Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gBDbNetSw2Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


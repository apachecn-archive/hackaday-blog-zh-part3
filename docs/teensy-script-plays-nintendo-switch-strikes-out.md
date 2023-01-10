# Teensy 剧本扮演任天堂 Switch，三振出局

> 原文：<https://hackaday.com/2017/10/25/teensy-script-plays-nintendo-switch-strikes-out/>

塞尔达系列的最新作品*《荒野之息*，因其众多谜题而闻名。其中一个更令人沮丧的是在山坡顶上用一个巨大的雪球打保龄球。[Bertrand]不喜欢这样，所以他~~欺骗了系统~~黑了任天堂 Switch，这样他每次比赛都“真正赢得”一击。他通过[为一个小小的模块写了一个脚本，让他得到了那些甜蜜的卢比](https://medium.com/@bertrandom/automating-zelda-3b37127e24c8)，从而实现了这个目标。

Teensy 内置 Atmel 90USB1286 微控制器。当与 [LUFA](http://www.fourwalledcubicle.com/LUFA.php) 软件配对时，它可以模拟许多控制器，包括键盘、操纵杆等。它还有一个位于其后部的 Mini-B USB 连接器，允许它轻松地与交换机通信。在确认硬件兼容后，[Bertrand]注意到已经存在的东西和他试图完成的东西之间的相似性，就把目光投向了软件方面。他在一个允许玩家写帖子的 Splatoon 2 fork 中偶然发现了这一点。

本质上，它将图像文件作为输入，并模拟控件和按钮来自动绘制图像的 1 位版本。这负责同步硬件以及如何模拟按钮按压。但是它需要接受一个自定义脚本作为输入，而不是读取一个图像文件。这需要从零开始。第一个合乎逻辑的步骤——当然——是创造一种类似于 [Logo](https://en.wikipedia.org/wiki/Logo_%28programming_language%29) 的语言，这个名字肯定会让人想起长发和垫肩的时代。他只需要几个简单的命令来控制 Link:

```

typedef enum {
	UP,
	DOWN,
	LEFT,
	RIGHT,
	X,
	Y,
	A,
	B,
	L,
	R,
	THROW,
	NOTHING,
	TRIGGERS
} Buttons_t;

```

值得注意的是，THROW 和 TRIGGERS 是复合命令，这意味着它们同时充当多个按钮。这解决了在向前轻推模拟操纵杆以投掷雪球时按下 R 按钮的问题，以及通过同时按压 L 和 R 触发器来解锁屏幕。然后，脚本被费力地手工输入，直到找到罢工的最佳条件。一旦捕捉到这些测量值，就会添加导致迷你游戏的整个对话的脚本，以实现一个循环，允许迷你游戏不停地重复播放。在不到一个小时的测试时间里，林克成功地连续打出了 22 个好球。[Bertrand]发布了所有的指令和源代码,这样每个人都有平等的机会从可怜的 Pondo 那里骗走卢比。

 [https://www.youtube.com/embed/udo8mv5oarg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/udo8mv5oarg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


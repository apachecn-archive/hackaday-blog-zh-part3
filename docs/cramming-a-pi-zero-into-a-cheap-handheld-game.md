# 把一个圆周率零塞进一个廉价的掌上游戏

> 原文：<https://hackaday.com/2018/01/25/cramming-a-pi-zero-into-a-cheap-handheld-game/>

在这一点上，我们已经看到树莓 Pi 被塞进了每一个复古的游戏系统，无论是手持的还是其他的。虽然它们总是有趣的构建，但总会有人对原始硬件必须被挖空来创建它感到不安。似乎每一篇帖子都会让一个经典游戏爱好者更加心碎。没有人会停止对游戏机的无谓屠杀吗？

碰巧的是，并不是所有的硬件改造者都是这种丧尽天良的畜生。[Starfire]最近将他的最新创作发送到了 tip line，它是专门为解决经典游戏屠杀而设计的，在这场游戏屠杀中，Hackaday 可耻地成为了合作者。他的构建牺牲了一个由 AtGames 构建的便携式 Genesis，而[将它变成了一个 Raspberry Pi Zero 便携式 running RetroPie。](https://www.youtube.com/watch?v=cbNdATdVQCk)

打开他的便携式 Pi 的后面板，可以看到在这个小小的包装里塞进了数量惊人的硬件。除了显而易见的 Pi Zero，还有一个 iUniker 2.8 英寸液晶显示器，一个 2200 毫安的电池，一个双端口 USB 集线器，一个 Teensy 微控制器，一个 USB 声卡，一个音频放大器，一个 LiPo 充电模块和一个升压转换器。[Starfire]测得的峰值功耗为 500 毫安，使用 2200 毫安的电池应该可以运行 3.5 小时。

当你意识到原来的 AtGames PCB 仍然在系统中时，这就更加令人印象深刻了，尽管中心被切掉以适合 Pi 的 LCD。[Starfire]不需要找出一种新的方式来处理输入，而是简单地将现有的输入连接到 Teensy 上的数字引脚，并使用一些代码将其转换为 Pi 的 USB HID。一些情况下的修改是必要的，即删除电池舱从背板和掩盖原来的 SD 卡插槽和端口；但除此之外，成品看起来完全是库存。

如果你不介意[变成一个真正的游戏男孩来制作你的便携式 Pi](https://hackaday.com/2016/11/12/pi-zero-transforms-to-game-boy/) ，你可以看看[的几个突出的例子](https://hackaday.com/2016/04/10/gameboy-case-lives-on-with-a-pi-zero/)，我们过去已经在这里报道过。

 [https://www.youtube.com/embed/cbNdATdVQCk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cbNdATdVQCk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


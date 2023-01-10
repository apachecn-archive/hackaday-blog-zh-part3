# 珊莎 MP3 播放器无法播放《毁灭战士》

> 原文：<https://hackaday.com/2016/12/30/sansa-mp3-player-runs-doom-unplayably/>

杜姆，有什么是它不能运行的吗？是的。你前面的草坪现在不能玩毁灭战士。不过，几乎所有其他东西都可以。这证明了游戏对社会的影响，它被移植到几乎每一个有按钮和图形屏幕的平台上。

这个视频展示了一段[珊莎扮演末日](https://www.youtube.com/watch?v=1rVV_0xKmhw)的片段，但只是勉强可以辨认。Sansa 剪辑有一个单色屏幕，顶部是黄色像素，屏幕的其余部分是灰色。单色显示器使事物难以看清，因此使用抖动技术来尝试使事物更加清晰可见。不幸的是，它不是特别有效，而且除了屏幕底部的枪之外，很难辨认出更多的东西。

这项特技是通过使用 RockBox(T1)来实现的，rock box 是一种为从苹果到东芝的各种媒体播放器定制的固件。通过不小的努力，开发者可以对不同的媒体播放器进行逆向工程，通常是通过拆卸硬件和固件。通常，第一步包括确定控制器的品牌和型号，以及确定如何访问其编程引脚&如何绕过任何可能存在的固件保护。有了这些知识，他们就可以着手移植 RockBox 代码了。这个项目投入的精力是惊人的，仅仅一个 Rockbox 港口的[文件就证明了这一点。](https://download.rockbox.org/daily/manual/rockbox-archosfmrecorder.pdf)

[Rockbox 还支持插件添加功能](https://www.rockbox.org/wiki/PluginIndex)。其中之一是 Rockdoom，它作为一个基本的 doom 引擎，可以加载 WAD 文件并玩游戏。因此，如果你热衷于复制黑客，首先把 Rockbox 移植到你的媒体播放器上，然后下载 Rockdoom 插件。

对于在一个不知名的平台上运行的定制固件的另一个很好的例子，请查看 [[Sprite-TM]关于入侵硬盘控制器芯片的演讲](http://hackaday.com/2013/08/02/sprite_tm-ohm2013-talk-hacking-hard-drive-controller-chips/)。

 [https://www.youtube.com/embed/1rVV_0xKmhw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1rVV_0xKmhw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Itay 的提示！]
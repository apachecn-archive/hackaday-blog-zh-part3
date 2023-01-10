# Arduino 中所有游戏精灵的国王

> 原文：<https://hackaday.com/2017/11/20/dual-port-ram-nes-cartridge/>

虽然任天堂正在怀旧的旧游戏机上大赚一笔，但仍有一小群专注的黑客在使用原始设备。尽管最初的 NES 是在 80 年代推出的，但这项技术还是有一些缺点。不过，现在我们有了 Arduinos、廉价的内存和有趣的工具链。我们能用这个做什么？绝对是我们想要的任何东西，比如在这个过时的系统上玩现代视频游戏。给他古老的 NES 控制台增加了双端口内存，为使用 NES 作为 Arduino 的视频终端打开了大门。当然，这也是所有游戏天才中的王者，也是一个有趣的周末项目。

大多数 NES 墨盒有两个内存位，PRG 和 CHR ROMs。[uXe]正在将盒式连接器连接到一根特别宽的彩虹带状电缆上，并将其放入一个定制的 Arduino Mega shield 中，该 shield 装载了两个 16K 双端口 RAM 芯片。这些 RAM 芯片有效地取代了 PRG 和 CHR ROMs，因为它们是双端口 RAM 芯片，它们可以同时被 Arduino 写入和被 NES 读取。

NES 可以看到 RAM 的一个端口，并可以读写它，而 Arduino 仍然可以在发生这种情况时对另一个端口进行更改。像这样的技巧打开了一个可能性的世界，最明显的是平铺和其他图形技巧，可以超越控制台的原始功能。[uXe]目前正在 NES 玩 Arduboy 游戏——一个非常巧妙的把戏。干得好[uXe]！

一定要看看下面的视频，NES 从 Arduboy 系统运行一些[游戏。它似乎可以无缝集成到硬件中，所以如果你一直渴望修复一些你最喜欢的游戏上的蹩脚图形，或者在 NES 上运行一些特殊的软件，现在可能就是你大放异彩的时候了。](https://hackaday.com/2015/08/18/arduboy-classic-plays-on-original-game-boy-screen/)

 [https://www.youtube.com/embed/OAwb10NGNno?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OAwb10NGNno?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


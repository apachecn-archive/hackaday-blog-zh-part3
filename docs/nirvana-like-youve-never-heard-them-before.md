# 涅槃就像你从未听过他们一样

> 原文：<https://hackaday.com/2016/07/13/nirvana-like-youve-never-heard-them-before/>

如果你是 20 世纪 90 年代初的年轻人，很有可能[涅槃乐队]的*闻起来像《少年精神》*是那种让你直接回到那个时代的音乐。作为你的作者，它让人想起一个学生广播工作室和它的唱片图书馆的书架，还有震耳欲聋的灯光昏暗的迪斯科舞厅，糟糕的扩音系统和令人讨厌的黏糊糊的舞池。

因此，我们今天早上的一个发现是一个令人回味的转移，*闻起来像[SileNT]的 Floppotron 上的青少年精神*。软盘驱动器是[一种由大量软盘驱动器、硬盘驱动器和几个平板扫描仪组成的音乐播放器](http://silent.org.pl/home/2016/07/06/return-of-the-floppies/)。扫描仪由现成的 Arduino 板控制，硬盘上有 ATMega16s 和 H 桥驱动程序。

这是我们见过的最精致的软驱风琴。软盘被分成由 ATMega16 控制的 8 个单音块，动态音量包络由同时运行的驱动器数量决定，因此声音可以像“自然”乐器一样渐入渐出。硬盘驱动器和扫描仪运行对他们的机械停止，提供打击。所有的板都通过 SPI 串行连接到 Arduino，Arduino 充当 PC 接口，PC 通过 Python 脚本调度性能。

他提供了几个 YouTube 视频，软驱马达对[涅槃]的垃圾音乐特别好用，但对夏威夷五零特遣队来说可能更机械一点。如果你在英格兰北部的一所大学上学，这最后一首歌会比第一首更令人回味，在那里，当一家迪斯科舞厅的灯光亮起时，播放的是深夜唱片，这家舞厅有一个调节得更好的 PA，因为技术人员知道她在做什么。对于那些有着不同童年的人来说，还有帝国进行曲。

 [https://www.youtube.com/embed/GwuCQ3u2N_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GwuCQ3u2N_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/32kWuKysE6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/32kWuKysE6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/Oym7B7YidKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Oym7B7YidKs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这些年来，我们在这里推出了许多软驱音乐播放器，尽管这是其中一个比较好的。几个亮点是[一个非常好执行的八驱动单元](http://hackaday.com/2014/01/05/the-most-beautiful-floppy-disk-jukebox-ever/)和一个使用 Arduino 的[从头到尾的构建。有趣的是，我们也看到一些](http://hackaday.com/2013/02/13/building-a-six-channel-floppy-drive-synth-from-start-to-finish/)[软盘驱动器被用作音频采样器](http://hackaday.com/2012/04/12/floppy-drive-as-an-audio-sampler/)，在一个相关的说明。
# 模拟完整的 Commodore 64

> 原文：<https://hackaday.com/2018/03/28/emulating-a-complete-commodore-64/>

当 Commodore 64 于 1982 年发布时，它是一个工程杰作。它的性能远远超过其他家用电脑，这都是因为 C64 内部有两个奇特的芯片。C64 的视频芯片 VIC-II 有精灵和滚动条，都被塞进了一个硅片里。SID 芯片是一个完整的片上合成器。这些硅片使 C64 成为有史以来最畅销的计算机，但也阻碍了在微控制器上模拟完整的 C64 系统的努力。

[弗兰克·博辛]刚刚成功地用一个小小的 3.6 秒模拟了整个 C64。Teensy 使用了一个异常强大的微控制器，但这是一个爱和代码的劳动。

这个项目的灵感来自一个反向工程的 SID 芯片[，它被移植到 Teensy 3.2](https://github.com/FrankBoesing/Teensy-reSID) 上。SID 芯片是任何 C64 仿真的成败关键，但是 Teensy 3.2 没有足够的 RAM 用于最新版本的 reSID。随着 Teensy 3.6 的发布，[Frank]认为增加的 RAM 数量将允许一个完整的 C64 系统，所以他构建了它。

新的 C64 仿真器使用 Teensy 3.6，带有一个小的附加“屏蔽”(或者不管我们叫它们什么)，为操纵杆和 Commodore IEC 总线提供连接器。有音频输出，支持 USB 键盘，支持 IL9341 SPI 显示器或常规的' ol VGA 显示器。

这个 Commodore 模拟器的整个开发过程都记录在 PJRC 论坛的[上，所有代码](https://forum.pjrc.com/threads/46168-queued-Commodore-C64-Emulation-on-a-Teensy-3-6-Microcontroller)[都在 GitHub](https://github.com/FrankBoesing/Teensy64) 上。这是一件了不起的作品，正如视频(如下)所示，这是一个真正的 Commodore 64，适合你的口袋。

 [https://www.youtube.com/embed/CjijgL0VC6k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CjijgL0VC6k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


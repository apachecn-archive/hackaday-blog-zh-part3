# MIDI 不仅仅是音乐，灯光秀怎么样？

> 原文：<https://hackaday.com/2018/03/31/theres-more-to-midi-than-music-how-about-a-light-show/>

如果你想在一个项目中结合你对音乐和电子的兴趣，MIDI 乐器和控制器是很有趣的设备。将音乐分解成标准化的数字信号，在技术上可以将任何带有按钮或传感器的东西变成乐器或效果踏板。另一方面，MIDI 信号的接收端大多被忽略。

[FuseBerry]是一位拥有电子和计算机科学背景的音乐鉴赏家，他一直想打造一个定制的 MIDI 设备，但他最终发明的不是乐器，而是一个 MIDI 控制的灯光表演，形状是一个爆炸的[截头二十面体](https://en.wikipedia.org/wiki/Truncated_icosahedron)([fuse berry]努力寻找这个名字不应被忽视)。他设计并 3D 打印了所有单独的几何形状，并煞费苦心地为它们配备了来自 WS2818B 条带的 led。Arduino Uno 控制这些 LEDS，并通过连接到 Arduino UART 接口的常规 5 针 DIN MIDI 连接器接收 MIDI 信号。

led 被映射到预定义的 MIDI 音符，因此无论何时播放其中一个音符，并且接收到它们的音符开信息，led 都会相应地点亮。[FuseBerry]使用他的 go-to DAW 来创建光模式，但任何可以发送 MIDI 信息的软件/设备都应该可以做到这一点。在项目的当前状态下，灯光图案需要手动创建，但对 Arduino 代码进行一些调整，这可能会更加自动化，[类似于这个 MIDI 控制的圣诞灯光秀](https://hackaday.com/2017/02/01/a-very-midi-christmas-lightshow/)。

 [https://www.youtube.com/embed/bkmGttRCtrw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bkmGttRCtrw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


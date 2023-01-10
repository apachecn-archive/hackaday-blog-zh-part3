# 按下按钮，用 MIDI 战斗机创作音乐

> 原文：<https://hackaday.com/2017/09/25/push-buttons-create-music-with-a-midi-fighter/>

如今，音乐家们有一系列的电子工具来帮助创作音乐。其中一些本身就是乐器，而[伟伦]——受 Choke 和 Shawn Wasabi 的启发——为自己打造了一个 midi 战斗机

Midi fighters 是可编程的乐器，其中每个按钮可以是音符、声音字节、效果或任何其他可以由按钮触发的东西。[Lun]的是由运行 Arduino 库的 ATmega32u4 控制的——闪存被识别为达芬奇——并且与许多音乐制作程序兼容。他选择了阳极氧化铝印刷电路板，以消除插拔时的弯曲，并赋予设备更精致的外观。休息之后，请查看实际情况！

[https://player.vimeo.com/video/233169523](https://player.vimeo.com/video/233169523)

[Lun]在 Fusion 360 和 KiCad 中设计了这个项目，为一些电子艺术留出了足够的空间——不得不喜欢[蠢朋克](https://hackaday.com/2016/09/06/a-helmet-to-make-daft-punk-jealous/)。他使用三和 OBSC 24 毫米街机按钮，以获得优质的质量，并使用两个 SK6812 迷你 led，当他们被按下时，产生光滑的照明效果。

在收到制造好的电路板和零件后，一个快速的测试装配直接进入最终装配。随着 ATmega32u4 闪烁和[编程](https://github.com/w4ilun/midifighter)，他准备好摇滚了。最终，[Lun]希望有一个 GUI 来配置每个按钮播放的音符，而不需要修改代码，但目前它工作得很好。

对于一个惊人的声学到电子乐器的转换，看看这个 [MIDI 手风琴](https://hackaday.com/2017/02/01/converting-an-acoustic-accordion-to-midi-oh-the-complexity/)！
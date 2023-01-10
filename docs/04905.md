# 一场非常 MIDI 的圣诞灯展

> 原文：<https://hackaday.com/2017/02/01/a-very-midi-christmas-lightshow/>

圣诞彩灯随着音乐闪烁肯定会在 YouTube 上增加浏览量并惹恼你的邻居。受一个这样的视频的启发，[阿克谢·詹姆斯]搭建了自己的展示，并在这个方便的教程中对这个过程进行了分类，让你开始自己的下一个假期。

[James]使用数字音频工作站 Studio One 获取歌曲《钟声激越》的 MIDI 数据，并将其用作该项目的 Arduino 大脑的灯光控制器数据。Studio One 通过[无毛 MIDI 转串行桥](http://projectgus.github.io/hairless-midiserial/)将歌曲的 MIDI 数据发送到 Arduino，Arduino 依次将相应的位设置为开或关。这将传递到三个 74HC595 移位寄存器，以及它们各自的三个继电器板，最终触发灯串的继电器。

接下来，就是给 Arduino 移位寄存器板、继电器布线，并连接灯光。哦，一定要在户外安装一个扬声器，以便路人可以欣赏音乐:

 [https://www.youtube.com/embed/UYB8DvlqYI8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UYB8DvlqYI8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



确保为继电器设置辅助电源，因为从 Arduino 获取电源可能会导致大问题。如果您的首选数字音频工作站没有虚拟 MIDI 乐器，[James]使用 loopMIDI 来获得想要的效果。他还提供了代码,如果你是在一个总是很忙碌的假日季节开发这个软件，他会帮你省去一些麻烦。

当然，你可以随时将灯插入物联网电源棒，享受其中的乐趣。
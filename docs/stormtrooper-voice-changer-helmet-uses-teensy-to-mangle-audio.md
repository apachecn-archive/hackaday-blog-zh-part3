# 冲锋队变声器头盔使用 Teensy 来破坏音频

> 原文：<https://hackaday.com/2016/11/09/stormtrooper-voice-changer-helmet-uses-teensy-to-mangle-audio/>

万圣节来了又去，但是这个由肖恩·海默尔制作的 DIY 变声星球大战冲锋队头盔教程值得一看。不仅整个事情是完全独立的，而且由于 [Teensy 的](https://www.pjrc.com/teensy/)强大的[音频过滤能力](http://www.pjrc.com/teensy/td_libs_Audio.html)，变声是在软件中完成的。此外，Teensy 还负责在变声演讲周围添加标志性的 Stormtrooper 点击、弹出和静态突发。看看下面的视频，听听它是如何工作的。

除了麦克风和扬声器，还有一个 Teensy 3.2，这是一个针对 Teensy 的低成本附加板，包括一个小型音频放大器和一个电源……仅此而已。看不到独立的 WAV 板或被黑掉的 MP3 播放器。

 [https://www.youtube.com/embed/Dyp3EyIlU4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Dyp3EyIlU4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在一个项目中让一切都很好地适应需要规划，不仅整个系统在头盔中是独立的，甚至还有管道风扇来帮助避免热衰竭。整个事情做得很漂亮，很好地展示了青少年在应用音频过滤能力方面的能力。

我们过去已经见过使用 [Raspberry Pi + USB 声卡](http://hackaday.com/2015/10/30/raspberry-pi-halloween-voice-changer/)的变声器，甚至还有 [Arduino + WAV shield](http://hackaday.com/2012/10/12/arduino-voice-changer-turns-you-into-vader/) 的变声器，但在头盔中完全独立的基于 Teensy 的单元还是第一次。

[via [Sparkfun 博客](https://www.sparkfun.com/news/2217)
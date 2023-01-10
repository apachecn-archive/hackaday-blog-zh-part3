# 复音调频合成器使用 ARM

> 原文：<https://hackaday.com/2015/12/14/polyphonic-fm-synthesizer-uses-arm/>

音乐家和会编程的人之间似乎有直接的关联。即使是不演奏乐器的程序员也经常对音乐有深刻的欣赏，所以我们看到相当多的音乐项目出现。最近的项目就是一个很好的例子。他结合了一个 STM32F031 ARM 开发板、一个音频编解码器和一个简单的运算放大器滤波器，使[成为一个可播放的 MIDI 乐器](http://blog.kehribar.me/build/2015/12/06/polyphonic-fm-synthesizer-with-stm32f031.html)。当然，很难从一张图片中欣赏一个音乐项目，但如果你想听结果，[总有 Soundcloud](https://soundcloud.com/ihsankehribar/wandering) 。

他用一个 8 位微处理器开始了这个项目，但是遇到了一些限制。他换了一款 STM32F031，这是一款低端 ARM Cortex M0 芯片。[Ihsan]提到他本可以使用内置于更大的 ARM 芯片中的 DSP 指令，但他希望在最少的硬件上完成项目。音频编解码器芯片来自 Cirrus Logic (a WM8524)，它产生两个 192 kHz 的输出通道。一个意想不到的好处是，编解码器使用电荷泵来产生负电压(很像 MAX232)，并且[Ihsan]能够利用该电压为音频滤波器中的运算放大器提供负供电轨。

该项目有很好的文档，并使用光隔离的 MIDI 接口。ARM 和编解码器之间的传输使用 DMA，而[Ihsan]使用一个有趣的技巧来模拟 ARM DMA 通道上的双缓冲(并很好地利用了“半完成”中断)。目前的设计可以做八个音符的复调，尽管[Ihsan]说通过修改代码可以做得更多。原型制作完成后(见上图)，他将电路移至专用 PCB，并将布局包含在项目文档中。

我们已经看到了很多有趣的 MIDI 项目，包括[黑色 MIDI 音乐](http://hackaday.com/2015/11/12/black-midi-there-is-no-denser-music/)甚至[无线 MIDI](http://hackaday.com/2015/07/17/transmitting-midi-signals-with-xbee/) 。[Ihsan 的]项目将是一个很好的 MIDI 启动项目，[听起来也很棒](https://soundcloud.com/ihsankehribar/daft-synth-stereo)。
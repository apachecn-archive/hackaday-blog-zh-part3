# MIDI DAC 用于老式合成器黑客

> 原文：<https://hackaday.com/2017/01/09/midi-dac-for-vintage-synth-hacks/>

许多经典合成器依靠模拟控制电压来改变参数；对于现代音乐家来说，这是一个问题，他们可能想要将这样的硬件与 MIDI 设置集成在一起。正是针对这个问题，【little-scale】内置了[一个 MIDI 可控的 DAC，用于产生控制电压](https://www.youtube.com/watch?v=wa4Z6aX7JL8)。

这是一个足够简单的构建——Teensy 2 用于对笔记本电脑讲 USB MIDI。这使得该 DAC 几乎可以与任何现代的支持 MIDI 的软件配合使用。然后，Teensy 通过 SPI 控制一个微芯片 MCP4922 来产生必要的控制电压。[little-scale]的视频介绍了硬件在试验板上的基本装配，并继续演示了如何使用 MIDI DAC 控制 Moog Mother 32 synth。[little-scale]也让代码变得可用，让你自己的代码变得更容易。

我们可以看到，这个项目对于与模块化合成器一起工作的电子音乐家来说是不可或缺的，这使得他们更容易在自己选择的 DAW 中与自动化联系起来。这也不是我们看到的第一个 MIDI 接口黑客——看看这个将 iPad 连接到吉他踏板的设置。

 [https://www.youtube.com/embed/wa4Z6aX7JL8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wa4Z6aX7JL8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


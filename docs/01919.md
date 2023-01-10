# ATtiny MIDI 插头合成器

> 原文：<https://hackaday.com/2016/03/30/the-attiny-midi-plug-synth/>

MIDI 创建于三十多年前，用于将电子乐器、合成器、音序器和计算机连接在一起。当然，这意味着 MIDI 本来是用于已经有 30 年历史的计算机，现在即使是最小的微控制器也有足够的处理能力来接收 MIDI 信号并创建数字音频。[mitxela]为 ATtiny 2313 设计的[复音合成器就是这么做的](http://mitxela.com/projects/polyphonic_synth_cable)，仅使用两千字节的闪存，并安装在一个 MIDI 插孔内。

将 MIDI 合成器插入 MIDI 插头是我们以前见过几次的事情。事实上，[mitxela]几个月前用 attin y85 做了同样的事情，[[Jan Ostman]的 DSP-G1](http://hackaday.com/2014/06/14/an-arm-based-dsp-modelling-synth/)用一个微小的 ARM 芯片做了同样的事情。不过，用 ATtiny2313 制造其中一个真的是挑战极限了。只有 2 kB 的闪存和 128 字节的 RAM，在这个芯片中没有太多的空间。制作一个复音合成器插头甚至更难。

[mitxela]芯片的电路非常简单，电源和 MIDI 数据由 MIDI 键盘、20 MHz 晶体提供，音频输出由八个数字引脚和一堆电阻提供。没错，这只是一个方波合成器，复音仅限八声道。正如下面的视频所显示的那样，它是有效的。

它是一个好的合成器吗？不，不是真的。根据[mitxela]自己的断言，这不是任何事情的实际解决方案，死虫构造需要一个小时才能完成，synth 本身仅限于带有一些难看的量化的方波。这是一个开发独特的音频设备，特别是 hackey 的整洁练习，使它成为一个非常酷的构建。听起来还不错。

 [https://www.youtube.com/embed/xgJmhjM_Kpg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xgJmhjM_Kpg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


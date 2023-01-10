# 一堆电线变成了模拟合成器

> 原文：<https://hackaday.com/2017/02/24/a-mess-of-wires-turned-into-an-analog-synth/>

在 YouTube 上，[GumpherDM3]建立了一个我们很久以来看到的最伟大的音乐项目之一。这是一种独一无二的模拟合成器。它也将是独一无二的:没有人会想要复制这一堆电线和纸板，而它们已经被成功地变成了一件完整的乐器。

这种合成器的设计是你所期望的，它从 Minimoog 和 Korg MS20 等半模块化合成器中汲取灵感。这个合成器上有四个 VCO，两个用于音频，两个用于 lfo。一个四极低通滤波器、VCA 和两个包络发生器完善了构件的纯模拟部分。里面还有一个自动琶音器，这是一个非常棒的演示视频(如下)。

在内部，这是一个真正的模拟合成器，带有围绕 LM13700 跨导放大器构建的 VCO、滤波器和 VCA。构建日志显示，这些芯片在插入焊接到手线 perf 板的插座之前，分散在大约半打试验板上。这个合成器是一种独一无二的乐器——没有人会想把它做两次。

附加功能包括一个带有 MIDI 输入端口的 Arduino，它将 CV 信号发送到合成器的模拟部分。这个东西拥有你所期望的模拟合成器的一切，听起来也很不错。

 [https://www.youtube.com/embed/msIQIWeMnBE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/msIQIWeMnBE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


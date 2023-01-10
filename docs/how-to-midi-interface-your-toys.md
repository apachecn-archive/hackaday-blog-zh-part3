# 如何连接你的玩具

> 原文：<https://hackaday.com/2017/06/30/how-to-midi-interface-your-toys/>

世界上有许多玩具，其中许多能发出各种令人愉快或讨厌的声音来娱乐孩子们。如果你是一名音乐家，这些玩具可能会因其独特或有趣的声音而感兴趣。然而，由于它们的设计旨在玩耍而不是表演，实际上可能很难将玩具用作乐器。解决这个问题的一种方法是将玩具的声音记录到采样器中，但这不是唯一的方法。[【little-scale】在这里演示如何为你的玩具提供 MIDI 接口。](http://little-scale.blogspot.com.au/2017/06/interfacing-with-toy.html)

[little-scale]从讨论一个人与玩具互动的许多方式开始。这篇文章讨论了一个简单的按钮如何被一个继电器或多路复用器取代，并与各种其他设备接口来控制玩具。这是通过使用一个手机玩具来演示的，当按下按钮时它会发出声音。

Teensy 3.6 用于运行该节目，充当 USB-MIDI 接口，因此该玩具可以由像 Abelton 这样的音乐软件控制。它通过一个多路转换器连接到玩具的按钮上。玩具的扬声器被切断，而是用作音频输出，使玩具可以很容易地连接到其他音频硬件进行表演或录音。它也是通过一个数字壶来传送的，所以 MIDI 命令可以控制音量。一个电阻被用来控制玩具中的音高，所以它也被一个数字电位计取代，以允许样本音高被控制。

这个项目有令人难以置信的良好记录，在逐步完成玩具与数字世界的每个接口阶段之前，[小规模]首先拆除玩具并突出兴趣点。我们以前也见过一些[little-scale]的作品，即[这款用于控制复古合成器的 MIDI DAC。](http://hackaday.com/2017/01/09/midi-dac-for-vintage-synth-hacks/)休息后的视频。

 [https://www.youtube.com/embed/GCO8yKpbpw0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GCO8yKpbpw0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


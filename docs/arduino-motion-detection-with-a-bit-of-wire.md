# Arduino 运动检测，带一点电线

> 原文：<https://hackaday.com/2016/05/23/arduino-motion-detection-with-a-bit-of-wire/>

很可能我们中的许多人会在某个时候实验过运动检测器。我们的 Arduinos、Raspberry Pis、Beaglebones 或任何东西都将被连接到超声波或 PIR 板上，这些板将被询问它们对面前事物的看法。

[Connornishijima]无意中发现了一种用 Arduino 检测运动的不同方法，[他用一段简单的双绞线连接到 ADC 引脚并接地](https://www.reddit.com/r/arduino/comments/4ju56v/i_discovered_a_method_to_passively_detect_motion/)，可靠地产生读数，指示他(或他的猫)何时在它附近。他称这种效应为“电容性湍流”，并对其机制的建议持开放态度。他只能让它在 Arduino 上工作，其他带 ADC 的电路板不能。

频繁的黑客攻击功能 e [Mitxela]可能也[发现了类似的东西](https://mitxela.com/projects/a_tiny_theremin)，我们一直犹豫要不要写出来，因为我们不了解它，但现在它变得不可避免。

在这种情况下，不经过自己的实验调查就自信地说出自己的观点“肯定是……”总是很危险的。我们这些最初对树莓 Pi 2 光敏的想法嗤之以鼻，后来不得不收回前言的人有特别的理由记住这一点。但这是一个值得理解的有趣效应。我们猜测 Arduino 的[相当高的输入阻抗](http://electronics.stackexchange.com/questions/67171/input-impedance-of-arduino-uno-analog-pins)可能会使它对电源嗡嗡声敏感，如果你对带有唱机输入的音频放大器做同样的事情，当你的手接近电线时，你可能会听到扬声器中有明显的嗡嗡声。在没有市电的情况下，在树林中的离网小屋里尝试这个实验会很有趣。

如果你想试试他的实验，他已经把他的草图贴在了 Pastebin 上。他把视频放在休息时间的下面，用猫来演示这种效果。

 [https://www.youtube.com/embed/4KjB-HMuUs4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4KjB-HMuUs4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们喜欢看到人们用他们的微控制器 I/O 线来拓展可能的边界，这增进了我们作为一个团体的集体知识。我们已经看到有人用 ESP8266s 制作[电视发射机，不久前还有一个](http://hackaday.com/2016/03/01/color-tv-broadcasts-are-esp8266s-newest-trick/) [Raspberry Pi ADC 端口](http://hackaday.com/2016/02/28/rasberry-pi-analog-input-using-only-passive-components/)作为进一步的例子。拜托，让他们来吧！
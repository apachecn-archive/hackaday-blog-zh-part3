# 现代 DIY 调频收音机

> 原文：<https://hackaday.com/2017/03/22/modern-diy-fm-radio/>

过去，自己动手制作收音机很有趣！我们只需要拿到一个锗二极管，做一些线圈，用一个电阻和一根长电线作为天线，也许我们可以从那些旧的白色耳塞中获得一些声音。那是过去的事了。现在，我们有了 Si4703 FM 调谐器芯片，可以在 76–108 MHz 范围内调谐 FM 收音机，集成 AGC 和 AFC，由 I2C 控制，以及一系列其他缩写，似乎使整个 DIY 收音机制作过程过时。过去的挑战产生了我们现在赖以发展的行之有效的解决方案。

[Patrick Müller]的这个小项目是一个[现代无线电 DIY 教程](https://www.hackster.io/Notthemarsian/fm-radio-97715f)。利用 Arduino Nano 作为 Si4703 分线板的大脑和控制器，他构建了一个功能齐全的便携式 FM 收音机。一个小的有机发光二极管显示器让用户看到音量，频率，选定的电台，并仍有空间显示当前可用的电池电压。它有音量控制、电台搜索和四个按钮，可以快速访问记忆的电台。源代码显示了如何控制 Si4703 FM 调谐器芯片来满足您的需求。

至于 IC，并不是所有东西都是新的，[Patrick]仍然使用[好的旧 LM386 amp](http://hackaday.com/2016/12/07/you-can-have-my-lm386s-when-you-pry-them-from-my-cold-dead-hands/) 来驱动扬声器，到现在已经快 35 岁了。正如我们在演示视频中听到的，它仍然可以输出一些非常响亮的~~音乐~~声音！

 [https://www.youtube.com/embed/5hkRLzX0W3Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5hkRLzX0W3Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



遗憾的是，由于调频接收器的频带限制，你无法在这台上听到木星的声音。
# Gecho 袖珍合成器活套

> 原文：<https://hackaday.com/2016/12/26/gecho-pocket-synth-looper/>

[马里奥]给我们写了[他的合成器项目](http://www.gechologic.com/)，这是[目前在 Kickstarter](https://www.kickstarter.com/projects/967276512/gecho-loopsynth-a-modern-equivalent-of-the-music-b) 上。它看起来很好玩，正如你在 Kickstarter 页面上的视频中看到的那样。但它也是为了易于破解而构建的。

在硬件方面，它是一个小小的四层电路板，塞满了各种部件。核心是 STM32F4 微控制器和 DAC。事实上，这一构建受到了其他人在 STM32F4 发现开发套件上的工作的启发，该套件已被用于制作一些非常有趣的合成器设备。[Mario]的版本增加了两个立体声耳机输出，两个麦克风输入，两个用作控制输入的红外反射距离传感器，一些按钮和大量的 led。然后它会很好地利用所有这些资源。

固件还没开源(戳！戳！)但是看起来就要了。在他的博客上，[Mario]通过一个例子在现有的固件中添加了一个鼓机,所以看起来它是可以被破解的。

从单个微控制器中挤出大量 DSP 功能是一项壮举。在来自不同制造商的类似芯片上，【Paul Stoffregen】的 [Teensy 音频库](http://hackaday.com/2014/09/30/the-teensy-audio-library/)也可以做许多相同的事情。但是 Gecho 项目真正的魅力在于它已经内置了一些有趣的硬件特性，并且随时可以使用。对于你自己的音乐或音频探索来说，这是一个不错的起点。
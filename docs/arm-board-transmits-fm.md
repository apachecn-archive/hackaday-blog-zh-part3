# 臂板发射调频

> 原文：<https://hackaday.com/2016/03/16/arm-board-transmits-fm/>

电脑人和音乐家之间不仅仅是偶然的联系。自 1961 年一台 IBM7094 演唱歌曲《黛西·贝尔》以来，计算机就一直在创作音乐(后来激发了另一台计算机 HAL 9000 做同样的事情)。

【Vinod。S]想在 STM32F407 探索板上创作音乐，但他还想在自己的调频收音机上播放。[他做到了](http://blog.vinu.co.in/2016/03/stm32f407-discovery-board-as-100mhz-fm.html)，他的手法令人惊讶又直截了当。关键是发现板上的 ARM 处理器使用 8MHz 晶振，但在内部(使用锁相环或 PLL)产生 100MHz 系统时钟。这恰好是在调频广播波段的中间。通过一个备用输出引脚将信号从芯片中取出，就可以获得 FM 载波。

这很简单，但是一艘航母本身是不够的。你需要调频载波。【Vinod。S]以通常的方式播放音乐，并通过电阻将模拟信号输入晶体。通过一些实验，他发现了一个足以将晶体频率提升到 100MHz 的值，当该值增加到 100 MHz 时，就会产生所需的 FM 偏差量。你可以在下面看到整个过程的视频。

令人惊讶的是，这并不是一个新想法。早在计算机出现的早期，众所周知，调幅收音机会接收到正在运行的计算机发出的噪音，而正确的程序可以播放音乐。有一篇关于在一台老牛郎星上做这件事的文章(尽管这项技术早于此)，甚至还有一个关于这件事的视频(T2)。说到视频，有一段关于 IBM 电脑的视频激励着哈尔演唱了 1961 年的歌曲。

我们涵盖了许多面向音乐的项目，包括那些人类无法制作音乐的项目。[常规项目](http://hackaday.com/2015/06/12/samplerbox-uses-raspberry-pi-2-to-make-music/)也很多。提醒一句:从你的微控制器发出 100 MHz 的信号可能不会让你在你的国家的无线电监管机构中处于有利地位。我们会小心翼翼地把这样的东西设计成真正的产品，除非你确定你知道你能通过法律测试。

 [https://www.youtube.com/embed/-62rpIWL23I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-62rpIWL23I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


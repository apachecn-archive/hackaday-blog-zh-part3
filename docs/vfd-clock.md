# VFD 时钟只会说罗马尼亚语

> 原文：<https://hackaday.com/2016/08/24/vfd-clock/>

不缺乏时钟项目，但[niq_ro]有他自己的[使用真空荧光显示器(VFD)和 Arduino，以及一对 MAX6921 ICs。这些芯片是用来驱动 VFD 的，使用两个 IC 需要做一些工作。Arduino 不是一个很好的计时器，因此该时钟还使用了 DS3231 时钟模块以及湿度和温度传感器。](https://arduinotehniq.blogspot.ro/2016/08/itron-fg209m2-vfd-display-controlled-by.html)

时钟是罗马尼亚语的，尽管有一些不同文本的选项。你可以在 [GitHub](https://github.com/tehniq3/VFD_FG209M2_2MAX6921) 上找到代码，并可以在下面的视频中看到结果。

VFD 通常用于需要在户外阅读的地方。它利用阴极发光来产生光。该过程类似于 CRT，但电压较低。这些灯管有一个涂有荧光粉的阳极，阴极用电子轰击它，使荧光粉发光。VFD 有不同的颜色。

VFD 在钟表中很受欢迎，从看起来非常精致的[到与这款类似的](https://hackaday.com/2016/04/20/sprite_tm-gives-near-death-vfd-a-better-second-life/)，但带有 MSP430。如果你对 VFD 的底层接口感兴趣，我们[也讨论过这个问题](https://hackaday.com/2015/03/04/reverse-engineer-a-vfd-after-exploring-how-they-work/)。

 [https://www.youtube.com/embed/nxz6LBEmo2Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nxz6LBEmo2Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


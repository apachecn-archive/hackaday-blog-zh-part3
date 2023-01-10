# 新零件日:I2C 在，查理复用发光二极管出

> 原文：<https://hackaday.com/2018/01/29/new-part-day-i2c-in-charlieplexed-leds-out/>

看起来 Hackaday 上涉及的大多数电气工程都只关注一个问题领域:如何让一束 led 疯狂闪烁。有很多 LED 驱动器，但最近记忆中更有趣的一个来自 ISSI，它是一种芯片，可以将 I2C 变成一个 Charlieplexed LED 阵列。你可能见过这种芯片——is 31fl 3731——它的形式是一个 Adafruit LED 矩阵(T1)和某个白痴做的一些愚蠢的东西(T2)(T3 ),但有了它，你只能在一个阵列中获得 144 个 LED，如果你想要真正的 blinky bling，这还不够。

现在，ISSI 发布了一种功能更强的芯片，可以将 I2C 变成更多的发光二极管。[is 31fl 3741 将在一个 39×9 矩阵中驱动多达 351 个 LED](http://www.issi.com/WW/pdf/IS31FL3741_EB.pdf)，或者如果你真的很聪明，一个 18×18 单色 LED 矩阵。

该芯片的特性包括每个 LED 的反向/短路检测、8 位 PWM、调光功能、保证 LED 开启或关闭的去重影功能、可配置的行/列矩阵，以及一些您希望在 LED 矩阵驱动器芯片中看到的其他便捷工具。该系列中最令人印象深刻的芯片将以低于 2 美元/片的价格提供，2500 片订量，尽管与 IS31FL3731 不同，这种新芯片似乎只提供 QFN 封装。

从经验来说，这是一个非常棒的芯片，可以驱动一整船的 led，前提是你有一台取放机。是的，你可以手工焊接一个 QFN 和几百个 0402 发光二极管，但我不推荐这样做。我真的真的不推荐。也就是说，这是实现最大 blinky bling 的完美芯片，来自 ISSI 的新闻材料给了我们一个伟大的想法，即使用这些芯片中的一个作为 RGB LED 机械键盘的背光控制器。这是一个很好的应用，而且芯片也很便宜。

你可以看看下面 ISSI 的这个芯片的 blinky 演示视频。

 [https://www.youtube.com/embed/_iC9-QsKLT4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_iC9-QsKLT4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


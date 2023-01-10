# AVR Vs PIC，第 223 轮:打！

> 原文：<https://hackaday.com/2016/06/28/avr-vs-pic-round-223-fight/>

准备好战斗吧！[Thierry]用两个微控制器做了完全相同的 Hello-World 风格的[项目(现在技术上是由同一家公司](https://hackaday.io/project/11796-avr-vs-pic-the-case-of-the-candle)生产的[！)看看体验如何。](http://hackaday.com/2016/01/20/microchip-to-acquire-atmel-for-3-56-billion/)

然而，这不仅仅是一个 LED 闪光灯。他增加了光探测功能，这样它只在晚上才打开。它使用 Forest Mims 技巧，反向偏置 LED 并等待其内部电容放电。然而，关键是，它让芯片有事可做，而不是简单地休眠。

虽然他习惯使用 AVR，但[Thierry]更喜欢 PIC，因为它在空闲、清醒和进行一些计算时功耗都较低。这主要是因为 PIC 有一个板载低功耗振荡器，使其能够以 32 kHz 的频率运行，但也因为芯片的功耗通常较低。最后大概在动力上比 PIC 多了 10%的优势。

如果你能胜任这两种芯片中的一种，但不能胜任另一种，那么他的相同代码的两个版本将是开始熟悉另一种的好方法。我们真的很喜欢他的`isDarkerThan()`功能，它在 LED 放电期间大量使用两个芯片上的睡眠模式。老实说，在这个层次上，两者的代码相似多于不同。

(哦，你有没有注意到[Thierry]用回形针来装硬币盒？是黑客！)

令人惊讶的是，我们已经设法避免了偶尔在 PIC 和 AVR 粉丝之间爆发的交叉火力中的流弹。我们在之前已经报道过[的一场“枪战”，PIC 也赢了那一轮，尽管也是势均力敌。收购 Atmel 的微芯片会平息战火吗？让我们在评论区了解一下。我们已经准备好爆米花了！](http://hackaday.com/2013/03/10/another-salvo-in-the-pic-vs-avr-holy-war/)
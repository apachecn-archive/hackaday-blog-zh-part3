# 吹灭蜡烛闪烁发光二极管:火焰的死亡

> 原文：<https://hackaday.com/2017/01/05/blowing-out-a-candle-flicker-led-the-death-of-flame/>

有一天将不再需要火焰。[slider2732]制造了一种使用闪烁 LED 的蜡烛，你可以吹灭它。再小型化一点，我们就可以把它们完全集成到生日蛋糕蜡烛的大小里了(提示提示，黑客们！).

你可能见过这些蜡烛闪烁发光二极管。它们内部有一个小芯片，可以调节 LED 的光，使其像蜡烛一样闪烁。我们甚至报道了[Cpldcpu]在逆向工程中发现的东西，他首先在这里[进行逆向工程](http://hackaday.com/2013/12/16/reverse-engineering-a-candle-flicker-led/)，然后在这里[进行逆向工程](http://hackaday.com/2014/03/02/reverse-engineering-candle-flicker-leds-again/)。

slider2732 所做的是买一个电子蜡烛，使用一个实际上形状像火焰的发光二极管，并在“火焰”附近钻一个洞。他在洞后面嵌入了一个麦克风。它连接到一个 LM386 放大器电路，再从那里连接到一个 Arduino Pro Mini，所有这些都是由一个 LiPo 驱动的。正如你所料，[Arduino 代码](https://www.dropbox.com/s/zrkjvfhela3bae7/Candle_Snuffer.ino?dl=0)非常简单，只需观察放大器的引脚，并根据内部变量，打开或关闭 LED。我们真的很喜欢看不到任何电子设备，而且你实际上必须俯身向蜡烛顶部吹气才能吹灭它。你可以在下面的视频中看到这一点。

为了再次点亮 LED，他这样做，以便在 LED 关闭时吹它会再次打开它。对于我们这些老学生来说，这似乎有点奇怪，所以我们希望看到一种电子火柴，当你用它擦东西时会发光(带闪烁的 LED)，当靠近它时会点亮蜡烛的 LED。当然你也会吹灭电子火柴！如果你没有那么大的野心，带闪烁 LED 的打火机也可以。完成后提交到我们的提示热线！

 [https://www.youtube.com/embed/hqfx-45dH8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hqfx-45dH8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


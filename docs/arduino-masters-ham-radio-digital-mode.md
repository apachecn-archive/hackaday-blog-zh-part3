# Arduino Masters 业余无线电数字模式

> 原文：<https://hackaday.com/2015/09/13/arduino-masters-ham-radio-digital-mode/>

[jmilldrum]的 Si5351A 分线板真的很有用。他是一个 ham [NT7S]，Si5351A 可以产生从 8 kHz 到 160 MHz 的多个方波，因此它理所当然地将成为任何 RF 黑客的有用工具。他最近的成果是用 I2C 可控芯片实现了一个快速简单的 FSQ 信标。

FSQ 是一种相对较新的数字模式，它使用一种低速率的 FSK 来发送文本和图像，这种方式在困难的射频传播下非常稳定。有 32 种不同的音调用于符号，因此普通字符只需要一种音调。没有一个角色的音调超过两个。

Si5351A 可以轻松处理编码工作。由于输出是方波，因此您需要一个低通滤波器来将其传送到空中。[jmilldrum]还使用了一些相对较小的放大器来获得高达 20 瓦的输出。

你可能还记得，在之前，我们已经[讨论过【jmilldrum】在 Si5351A 上的工作。我们最近也在](http://hackaday.com/2014/06/27/generate-clocks-with-the-si5351-and-an-arduino/)[谈论 hams 试验数字模式](http://hackaday.com/2015/09/09/steal-this-ham-radio-technology/)，这是一个很好的例子，FSQ 和[jmilldrum]的开发者都用 Arduino 实现了它。如果你想更多地了解 FSQ，请看下面的视频。

 [https://www.youtube.com/embed/_j4qZJuWDcM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_j4qZJuWDcM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


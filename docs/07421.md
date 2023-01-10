# 福图:LED 灯条是可怕的伺服驱动器

> 原文：<https://hackaday.com/2017/10/19/fotw-led-strips-make-awful-servo-drivers/>

我们肯定都曾在某个时候发现过一个看起来不可思议的想法，而且只是*有*可以尝试，但结果却是将可能性的界限延伸得太远了，只是一个*小*。我们的一大块时间消失得无影无踪，我们不好意思地为手头的工作购买合适的零件。

[Orionrobots]与一位 YouTube 关注者就 LED 灯条进行了一次对话。他们认为，一个 LED 灯带包含一段现成的 PWM 驱动器。如果一个条上的每个驱动器都可以连接到一个伺服系统，那岂不是很棒，[使该条成为现成的单站 SPI 伺服驱动器](https://www.youtube.com/watch?v=U06c4os9Yuk)。随着一个大型多伺服机器人的建立，他开始在 WS2801s 上工作。

如果你是在焊接区，并在铁精英技能，然后焊接一条线到表面贴装驱动芯片是完全可能的。不过对于普通人来说，这是一个挑战，他注意到这给项目增加了多少额外的时间。虽然当伺服系统被连接起来时，乐趣就开始了，但最好的情况是它振动了一下。理论上，LED 驱动器应该能够驱动伺服系统，因为它们可以产生正确的波形。但实际上，伺服系统被设计为接受逻辑电平输入，而驱动器被设计为与 LED 串联并控制其电流。因此，在实践中，逻辑转换所需的电压无法完全达到。

他最后建议观众花在伺服驱动板上，而不是尝试 LED 灯条。我们为他的努力鼓掌，毕竟这是一个我们任何人都可能想到要自己尝试的技巧。

 [https://www.youtube.com/embed/U06c4os9Yuk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U06c4os9Yuk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


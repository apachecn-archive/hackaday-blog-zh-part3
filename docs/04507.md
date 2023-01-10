# 向卡西欧 PX410R 添加 MIDI 输出

> 原文：<https://hackaday.com/2016/12/28/adding-midi-out-to-the-casio-px410r/>

自 20 世纪 80 年代以来，MIDI 一直是在电子乐器之间发送数据的一种很好的方式。从通过光隔离器和 DIN 插座运行的改进型串行接口开始，如今，您的硬件更有可能通过 USB 传输 MIDI 数据。如果你想连接到一台没有笨重接口的计算机，这是很好的，但当你想把一堆仪器相互连接起来时，这就不那么好了。

Roland Integra 7 是一款带有经典 MIDI 端口的机架式合成器。[ 阿德里安金 ]想要通过 MIDI 控制合成器，但他们的卡西欧键盘只有 USB 上的 MIDI 可用。为了解决这个问题，[阿德里安金]着手[给卡西欧 PX410R](https://adriangin.wordpress.com/2016/12/19/casio-px410r-midi-out-hack/) 增加一个标准的 MIDI 输出端口。

如果你想成为一名硬件黑客，熟悉标准串行通信。在使用键盘的延音踏板时，在测试垫周围进行了一些探测后，[adriangin]发现了两个 IC 之间看起来像是 MIDI 信号的东西，但比特率不是标准的。直觉证明是正确的——信号在合成器 DSP 芯片和处理 USB 连接的 IC 之间传输。标准的 MIDI 接口工作在 31250 波特，而这个信号是 215500 波特。没有简单的方法可以从一种波特率转换到另一种，所以[adriangin]不得不艰难地完成。

Atmega32P 投入使用，使用在数字引脚上实现的软 UART，以 215500 波特运行。在如此高的比特率下，软 UART 需要一些周期精确的汇编编程来使一切正常运行。然后，数据将被转发到运行在 31250 上的硬件 UART，该硬件 UART 连接到经典 MIDI 中使用的标准 DIN 插头。这是一个有用的技巧，它允许键盘与更广泛的硬件一起工作。它干净利落的设计更胜一筹，新端口巧妙地集成在后面板中。

看看这些其他伟大的 MIDI hacks，像这个从头开始建造的[chip tune looper](https://hackaday.com/2011/12/23/bitbuf-delivers-some-of-the-best-chiptune-effects-around/)或者这个[支持 MIDI 的 Stylophone](https://hackaday.com/2011/11/15/stylophone-5-modernizing-the-best-of-the-1968-hardware/) 。
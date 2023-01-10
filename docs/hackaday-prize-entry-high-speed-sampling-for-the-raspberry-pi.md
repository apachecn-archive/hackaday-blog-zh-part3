# Hackaday 奖参赛作品:树莓 Pi 的高速采样

> 原文：<https://hackaday.com/2017/04/30/hackaday-prize-entry-high-speed-sampling-for-the-raspberry-pi/>

Raspberry Pi 因其一系列 GPIOs 和其他接口，以及其经济实惠的计算能力，已经成为我们社区中最受欢迎的产品。不幸的是，尽管有这么多引脚，但它的接口能力却明显不足。它没有模数转换器，所以模拟输入必须依赖那些 GPIOs 上的扩展卡或通过 USB 端口。

大多数人仍然满足于简单的 ADC，如微芯片的 MCP3008，或者用于低频移动目标的 USB 声卡。但不是[Kelu124]，他把目光投向了更快的东西。最初的 Pi 被认为能够处理 10 兆样本/秒的 ADC，所以他认为更快的后继者应该能够工作得更快。为此，[他创造了一个 ADC pHAT，他认为它应该是这个数字的两倍](https://hackaday.io/project/20455-20msps-adc-raspberrypi-extension-bomanz)。

选择的芯片是 CA3306E，这是一款 6 位器件，额定速率为 15Msamples/S，从其 DIP 封装可以看出，这是一款过时的器件，快速浏览一下主要供应商就可以发现，这款器件已经停产。不过令人高兴的是，当你看到他的 GitHub repo 时，你会发现他也在生产基于 ADC08200 的电路板，所以他的软件可以针对其他芯片。

无论您是否需要您的 Pi 作为视频数字化仪或高速仪器，看看这样一个电路板的运行情况都是有用和有趣的。我们经常不使用我们的单板计算机的原始能力，这个项目证明，如果我们需要，我们可以。

如果您对 ADC 感兴趣，可以看看[【Bil Herd】关于δ-σADC 的系列文章](http://hackaday.com/2016/07/07/tearing-into-delta-sigma-adcs-part-1/)。

谢谢[Fustini]的提示。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
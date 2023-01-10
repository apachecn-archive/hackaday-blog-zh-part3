# Hackaday 奖品入口:Arduino 的神奇线控运动检测器库

> 原文：<https://hackaday.com/2016/09/01/hackaday-prize-entry-magic-bit-of-wire-motion-detector-library-for-arduino/>

我们仍然不确定[connornishijima]的运动探测器到底是如何工作的，尽管上次我们报道时，许多读者在评论中提供了似乎合理的解释。不过，它工作得很好，他已经开始使用 Arduino 方式，并把它很好地打包成一个库。

在上一篇文章中，我们介绍了[connor] [演示](http://hackaday.com/2016/05/23/arduino-motion-detection-with-a-bit-of-wire/)运动检测器。Arduino 的 ADC 电路的连接方式使其工作。到目前为止，最不可能的理论涉及生命力，或者更确切地说，是来自《星球大战》的力。最有可能的理论是在电容和静电荷之间争论。

不管怎样，这是一个足够可靠的现象，他投入了承诺的时间，写了一个库。甚至还有关于 GitHub 的文档。要初始化该库，只需告诉它连接了哪个模拟引脚、本地交流频率是多少(这样就可以滤除其噪声)以及一个最终值，该值告诉 Arduino 在报告事件之前多长时间取平均值。

这看起来很有效，可能会很有趣，或者用你的魔法让你生活中的年轻黑客惊叹不已。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)
# Hackaday 奖参赛作品:中风后康复测力计

> 原文：<https://hackaday.com/2017/10/02/hackaday-prize-entry-dynamometer-for-post-stroke-rehabilitation/>

对于中风患者来说，康复是一个漫长而缓慢的过程，需要尽早开始康复。通常，二次中风会使事情复杂化。痉挛——肌肉收缩和轻瘫——肌肉无力，是中风的两种常见后遗症。恢复包括反复做练习来加强肌肉和恢复肌肉记忆。当护理人员只能使用定性手段(如挤压网球)来监测进展时，制定进展基准就变得很困难。为了帮助在这种情况下提供定量测量，[Sergei V. Bogdanov]正在建造一个用于中风后康复的[测力计](https://hackaday.io/project/26095-dynamometer-for-post-stroke-rehabilitation)。这是一个开源的 4 通道差分测力计，用于测量和记录患者的进展。当四个手指按下四个测力计时，该设备测量、绘制和记录四个手指施加的力。

该装置由四个从廉价厨房秤获得的应变仪组成。这些器件的模拟输出馈入 HX-711 24 位 ADC 板。Arduino Nano 处理数据，并将其显示在两组八位数的 LED 模块上。[Sergei]还尝试用 20×4 字符的 LCD 代替 LED 显示屏。在独立模式下，该装置只能在 LED(或 LCD)显示器上显示测得的力，该显示器被校准以显示数值或对数标度。当连接到串行端口并使用(仅适用于 Windows)程序时，不仅可以查看相同的信息，还可以按固定的时间间隔保存信息。数据也可以以图形形式查看。

项目页面提供了他们的 Arduino 代码、Windows monitor 程序以及构建说明的链接。查看[Sergei]正在进行的相关辅助技术项目— [中风后痉挛康复助手](https://hackaday.io/project/26963-post-stroke-spasticity-rehab-helper)。

 [https://www.youtube.com/embed/GuAnWTvea-4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GuAnWTvea-4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
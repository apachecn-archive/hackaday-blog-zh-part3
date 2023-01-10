# 变色时钟使用 PCB 数字

> 原文：<https://hackaday.com/2017/12/13/color-changing-clock-uses-pcb-digits/>

有一句老话，你应该做任何事情至少两次。第一次是学习如何做，第二次是做对。也许[Zweben]会同意，因为他不满意他的第一个 Neopixel 时钟，并继续建造另一个。吸取的一个教训是:焊接 180 个微小的焊点并不好玩。这一次，[Zweben]着手制作印刷电路板，重新设计时钟，使其更容易组装。

该时钟使用单个电路板的多个副本。该板将 Neopixel 条带排列成 7 段。每个电路板还可以容纳驱动时钟所需的所有电子器件。只有第一块板得到微控制器和其他电路。

这使得[Zweben]可以设计一个 PCB，他用 [EasyEDA](https://hackaday.com/2017/12/05/easyeda-two-years-later/) 设计了这个 PCB。硬件本身与他最初的时钟非常相似，软件不需要改动。

说到硬件，这个时钟是 Arduino Pro 迷你克隆和 DS3231 I2C 时钟的一个非常标准的混搭。Neopixel 条带是每米 60 个 WS2812B LEDs，每个数字段有两个 led。每个数字上总共有 14 个，整个时钟上有 58 个可单独寻址的灯。

这让我们想起[一个来自【decino】的类似时钟](https://hackaday.com/2017/11/01/bluetooth-bedroom-clock/)，他也厌倦了焊接连接。我们还喜欢使用 [Neopixel 环代替长条](https://hackaday.com/2016/12/02/7-segment-display-using-neopixel-rings/)的时钟。
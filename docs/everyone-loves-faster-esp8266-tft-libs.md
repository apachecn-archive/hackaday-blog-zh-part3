# 每个人都喜欢速度更快的 ESP8266 TFT Libs

> 原文：<https://hackaday.com/2017/04/08/everyone-loves-faster-esp8266-tft-libs/>

读者[Jasper]在文章中对 ESP8266 的 TFT_eSPI 库和各种廉价的 480×320 TFT 显示器(ILI9341、ILI9163、ST7735、S6D02A1 等)赞不绝口。)支持 SPI 模式。它是阿达果 GFX 和驱动程序库的替代产品，所以你不需要重新编写代码来利用它。如果你想用 ESP8266 和 Arduino 驱动一个 LCD 屏幕，请确认一下。

作为一个测试平台，[Jasper]将他的[滴答计时器](https://hackaday.io/project/6651-tick-tock-timer)项目移植到新的库中。他的绘制速度增加了七倍，从 500 毫秒增加到 76 毫秒。这就是明显缓慢的刷新和看起来像是立即发生的刷新之间的差异。太好了。

改善软件基础设施不是最性感或最明显的黑客行为之一，但它可以触及许多黑客的生活。我们有多少项目采用了 ESP8266 和屏幕？感谢[博德莫尔]的出色工作，感谢[贾斯帕]让我们注意到这一点。
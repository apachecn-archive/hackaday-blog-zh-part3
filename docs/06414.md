# ESP32 显示器胜过千言万语

> 原文：<https://hackaday.com/2017/07/03/esp32-display-is-worth-a-thousand-words/>

ESP32 是广受欢迎的 ESP8266 的继任者。芯片能做的事情似乎没有止境。然而，尽管有所有的无线通信能力，该模块没有显示器。[G6EJD]想要[连接一个 ILI9341 TFT 显示器](https://github.com/G6EJD/ESP32-and-how-to-use-ILI9341-TFT-Display)，他将代码和信息放在 GitHub 上。你也可以在下面看到他的工作视频。

因为显示器使用串行接口，所以不需要太多布线。Adafruit GFX 库完成了繁重的工作，利用 SPI 库进行实际通信。硬件上显示的第一个演示可以将天气数据解码。如果你想了解显示器操作的更多细节，请查看[G6EJD]YouTube 频道，你会找到其他更详细的视频。

我们已经看到这些显示器[与带有集成 PCB 的 ESP8266](https://hackaday.com/2016/08/17/nerd-bait-esp8266-ili9341-screen/) 结合在一起。有一个[选择库，](https://hackaday.com/2017/04/08/everyone-loves-faster-esp8266-tft-libs/)，也许我们会看到一个类似的 ESP32 的选择范围。

 [https://www.youtube.com/embed/cOH7vcLCKhE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cOH7vcLCKhE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# MicroPython 学会了一个新技巧——面向 AVR 的 ISP

> 原文：<https://hackaday.com/2018/01/18/micropython-learns-a-new-trick-isp-for-avrs/>

Arduino 如此受欢迎的原因之一是它能够轻松编程。这意味着大型并行程序员的终结，他们将付出高昂的代价。来自[Lady Ada]和 Adafruit 团队的 CircuitPython 的最新版本是一个用于在没有专用 PC 的情况下对 AVR 微控制器进行编程的库。

对于外行，AVR 控制器的系统内编程或 ISP 采用 SPI 总线将编译后的二进制文件写入控制器的闪存。使用引脚数量的折扣本身就是一个好处，尽管在过去的好时光里，获得正确的时序有点棘手。大多数专门的互联网服务提供商处理得很好，虽然他们通常是主机的奴隶，一个“上传”按钮启动这个过程。

有了 circuit python(MicroPython 的衍生产品)，微控制器编程不需要经历代码-编译-闪存循环。它可以在许多处理器上运行，然而，AVR 不在其中，所以这个整洁的小库提供了下一个最好的东西。将 Atmega328P 或 ATmega2560 连接到运行 CircuitPython 的 ESP8266 等电路板上，就可以动态编写固件。

多亏了[Phillip Torrone]和[Lady Ada],有一个关于这个主题的完整教程,其中包括一些测试功能的演示文件。这为 AVR 协处理器的 OTA 固件更新提供了许多可能性。我们期待在不久的将来看到一些钥匙链 AVR 程序员从之前的 [ESP8266 双因素认证](https://hackaday.com/2018/01/04/two-factor-authentication-with-the-esp8266/)中得到启示。
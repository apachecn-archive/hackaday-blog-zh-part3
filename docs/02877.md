# Hackaday 奖参赛作品:随时随地的电子产品

> 原文：<https://hackaday.com/2016/07/12/hackaday-prize-entry-electronics-anywhere-any-time/>

人们一直需要电子绘图纸——一种记录 1 和 0、写入位并跟踪模拟电压的数字设备。很久以前，这种装置*是*绘图纸，缠绕在一个鼓上，每天缓慢旋转一周。随着廉价、强大的微控制器和 SD 卡的出现，这些设备变得更加强大。

为了获得 Hackaday 奖，[Kuldeep]和[Sandeep] [建造了 Box0](https://hackaday.io/project/11074-box0) 。这是一个包里的实验室，一个开源的数据采集单元，和一个切换引脚的 USB 设备，所有这些都在一个简单的设备中。

该器件的硬件包括一个 STM32F0 微控制器、一个 USB 端口和足够多的引脚来提供几个 SPI、一条 I2C 总线、八个数字输出通道、两个 PWM 通道、一个 UART、模拟输入、*和*模拟输出。

当然，硬件是容易的部分。如果你想用这样的设备做一些有用的事情，你需要一些软件。这是这个项目真正闪光的地方。他们有 Python、Julia、C、Java 和 JavaScript 的库。这足以让任何人高兴，并使这个 Box0 格外能干。为了进行演示，他们用 Box0 为晶体管和[红色、绿色和蓝色发光二极管](https://hackaday.io/project/11074-box0/log/36906-red-green-blue-led-i-v-characteristics)制作了[曲线跟踪器。它起作用了，看起来这实际上是一个非常有用的设备。](https://hackaday.io/project/11074-box0/log/37672-building-a-transistor-curve-tracer)

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)
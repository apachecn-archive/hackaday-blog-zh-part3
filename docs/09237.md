# 剖析 AVR 调试线

> 原文：<https://hackaday.com/2018/04/24/dissecting-the-avr-debugwire/>

任何编写过十几行代码的人都知道，调试是我们生活的一部分。任何为微控制器写代码的人都知道物理调试也是我们生活的一部分。Atmel 处理器使用一种称为 debugWire 的串行通信协议，这是 JTAG 的一个简单版本，允许对所有寄存器进行完全读/写访问，并允许单步执行、中断等。[Nerd Ralph]是 Hackaday 的一位知名人士，他[深入研究了 AVR debugWire 协议](http://nerdralph.blogspot.ca/2018/04/debugging-debugwire.html)，并为我们提供了一些有价值的信息。

虽然 debugWire 的[协议方面是一个大部分已经解决的问题](https://hackaday.com/2016/04/07/reverse-engineering-debugwire/)，但是物理层给他带来了麻烦。他从一个二极管开始，然后经过几个电阻和其他元件，与 AVR 微控制器上的 debugWire 引脚接口，完成了大部分故障诊断工作，所以现在您不必这样做了。他指出，接口组件可能需要针对特定的 USB-TTL 适配器进行定制，所以如果您想亲自研究 debugWire，请记住这一点。

在 Hackaday，我们对[调试技术](https://hackaday.com/2018/02/12/stepping-up-your-python-printf-debugging-game/)并不陌生。一如既往，如果您遇到任何新技术或尝试任何新东西，一定要让我们知道！
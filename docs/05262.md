# 用 PROGMEM 保存 ESP8266 RAM

> 原文：<https://hackaday.com/2017/03/10/save-esp8266-ram-with-progmem/>

当[stitilface]开始使用 Arduino IDE 编写 ESP8266 时，他发现自己的 ram 很快就用完了。罪魁祸首？弦乐。这并不奇怪。字符串可以很长，而且许多字符串(如提示等)永远不会改变。有一种方法可以告诉编译器，你想把不会改变的数据存储在程序存储器中，而不是 ram 中。当然，它们仍然会消耗内存，但是你拥有的程序存储空间要比一个典型设备上的 ram 多得多。他把他的结果发布在一个网站上。

从表面上看，用 PROGMEM 关键字定义内存分配非常简单。还有使事情变得更简单的宏和一系列用于处理程序空间中的字符串的函数(基本上，标准 C 库调用带有 _P 后缀)。

然而，还有一个助手类，它允许您使用驻留在程序内存中的 string 对象。这使得使用这些字符串变得更加容易，尤其是当您将它们传递给函数时。例如，[stilface]编写了一个处理 PROGMEM 字符串的字符串连接函数。

您也可以对其他数据使用相同的技术，在本文的最后，有一些不同用例的非常清晰的例子。在引擎盖下，ESP8266 不在程序内存中以字节存储数据。库例程对您隐藏了这一点，但如果您试图计算空间或进行某种操作，这可能很重要。

你也可以查看官方文档。如果你想看看这项技术的实际应用，也许你会对[你同事的情绪](https://hackaday.com/2014/12/24/trinket-edc-contest-entry-can-i-borrow-a-feeling/)感兴趣。或者，试着在你的示波器上安装一个[扳手](https://hackaday.com/2011/08/01/want-to-play-pong-on-your-oscilloscope)。两个项目都使用 PROGMEM。

【编者按:PROGMEM 在 AVR-GCC 的 ESP8266 Arduino 代码库中，最初(违反直觉地)写入 RAM。一些聪明的黑客在去年早些时候修复了这个问题，所以现在你可以对 ESP 使用相同的 AVR 风格的抽象。在 ARM Arduinos 上还是不行。]

图片由[Connor good wolf]([CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0))
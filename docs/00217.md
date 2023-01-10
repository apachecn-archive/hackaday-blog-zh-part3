# KIM-1 时钟

> 原文：<https://hackaday.com/2015/09/29/kim-1-clock/>

在 hackaday.io 上，[Arduino Enigma]发布了他的时钟代码，该时钟运行在一个 KIM Uno(我们[去年年底提到的 KIM-1 克隆体](http://hackaday.com/2014/11/07/the-kim-1-computer-minified/))上。尽管 KIM Uno 已经预装了一些演示程序(包括 Microchess 和一个科学计算器)，但它们都需要一些交互。时钟使 KIM Uno 成为一个更加动态的桌面显示器，因为它在没有任何用户交互的情况下做一些有用的事情(当然，一旦你设置了时钟)。

项目显示的是存储在 ROM 中的代码，但是你不能直接把程序输入 ROM(其实就是主机 Arduino 上的 EEPROM)。诀窍是输入地址(即按 AD，然后按 0，4，0，0)，然后按住重置按钮大约一秒钟。然后，您可以按 DA 并输入提供的十六进制代码(在每个字节后按+)。由于代码在非易失性存储器中，你可以通过在 RAM 中设置时间并在地址 400 执行代码来随时启动它。

该计划是简短而甜蜜的，使它很容易进入和一个很好的机会来了解你的 6502。然而，简单意味着它不检查你的初始时间设置，所以不要告诉它是 32:99 或类似的东西。代码没有注释，但是一旦你意识到一件事，它就非常简单:第一条指令 SED 设置 6502 的十进制模式，所以不需要十六进制和十进制之间的转换。

时间的每一部分(小时、分钟和秒)都存储在 RAM 的 0024、0025 和 0026 位置。NEXTD 例程使用 X 寄存器扫描时间的每个部分，适当增加 1 或 0(存储在 RAM 位置 0029)。如果时间部分与 CARRYT 处的相应表格条目相匹配(即，60、60 或 24 也由 X 寄存器索引)，则代码不会转移到 CONTIN，而是将增量(位置 0029)重新加载为零，因此接下来的数字不会前进。如果匹配，增量保持为 1，当前零件返回零值。

您可能会注意到时间被存储回从 0024 和 00F9 开始的位置。这是因为当在 1F1F 调用 ROM 常驻子程序时，00F9 是 KIM-1 ROM 寻找数据写入显示器的地方。X 寄存器的范围从 0 到 2，对应于秒、分和小时。一旦所有的时间都被更新，L1 的环路显示时间并延迟大约一秒钟。

这是一段简洁的代码，也是 6502 十进制模式强大功能的一个很好的例子。这看起来会更好，有了 KIM-1 UNO 的增强版。

 [https://www.youtube.com/embed/Pqnz_kiXPJ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Pqnz_kiXPJ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


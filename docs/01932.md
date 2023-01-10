# 非常便宜的 USB Arduino 黑客从过去

> 原文：<https://hackaday.com/2016/03/29/dirt-cheap-usb-arduino-hack-from-the-past/>

大规模生产是一件美妙的事情。价格下降，爱好黑客得到便宜的装备。然后，思想会转向如何利用它。因此，难怪像[Aaron Christophel]这样的人会[试图重新利用那些遍布易贝的低于 3 美元的 AVR 程序员](http://atcnetz.blogspot.de/2013/10/2-arduino-bzw-usbasp-20-firmware-hack.html)([在这里从德语翻译出来很差](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=http%3A%2F%2Fatcnetz.blogspot.de%2F2013%2F10%2F2-arduino-bzw-usbasp-20-firmware-hack.html&edit-text=&act=url)，但在下面嵌入的视频中演示了)。

真的不需要做太多。唯一的诀窍是，你首先需要刷新现有的 ISP 固件，让你可以通过 USB 上传代码到设备本身。如果你手头没有 Arduino 来刷新，至少买两个便宜的程序员——一个给另一个编程。一旦你做到这一点，你基本上有一个 Arduino 有限的引脚和两个板载 led，但在一个漂亮的小外形和内置 USB。[Aaron]甚至提供了一个 Arduino`boards.txt`文件来使它在 IDE 中顺利工作。

所有这一切都是通过非常友好的 V-USB 固件来完成的，它可以让你廉价而简单地构建低速 USB 设备。这非常适合制作双按键键盘、USB-USART 或 USB-SPI 桥，甚至是音量控制旋钮——一个 ADC 引脚似乎坏了。通过一些微妙的焊接，其余的引脚可以被带出来，你可以用这个小电子狗做一些真正有用的事情。

甚至很难想象采购所有零件的成本有一个运送到你的门口，这是一个相当老的黑客，可以追溯到 2013 年。我们有点惊讶，我们没有看到更多的项目，人们重新利用这些廉价的 ISP 程序员。你用这个做过什么吗？让我们知道。

 [https://www.youtube.com/embed/vzxqYnSjbyU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vzxqYnSjbyU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


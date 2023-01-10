# 什么东西很小，有八条腿，行为像 Arduino？

> 原文：<https://hackaday.com/2016/03/27/whats-tiny-has-eight-legs-and-acts-like-an-arduino/>

早在 20 世纪 70 年代末，喜剧演员史蒂夫·马丁就说过“让我们变小吧！”在 Hackaday.io 上，[Daniel grie Haber]将这一呼吁铭记于心。他一直在研究 DIL-Duino ，这是一款 8 引脚 DIP 格式的微型 Arduino。

该板采用 ATtiny85 制造，面积不到 75 平方毫米(不到 8 毫米 x 10 毫米)。如果加上 USB 端口，它的面积仍然只有 144 平方毫米多一点。[Daniel]发现其他小 Arduino 板，如 Olimexino-85s 和 Nanite，都没有他的设计小。

该模块有一个 QFN CPU 和周边用于安装的堞形孔。有了引脚接头，这将很容易安装到试验板上(如[Daniel]所示),或者你可以像表面贴装器件一样直接将其安装到另一块板上。事实上，这就是使用堞形孔的原因:您可以检查配套 SMD 焊盘的焊点是否良好。你有时会听到这种技术被称为半通孔或无引线芯片载体。

如果你注意到，[丹尼尔]使用了一个超大的板，周围全是孔，然后让板制造商在板上划线，所以孔被切成两半。这是一种比试图在木板边缘钻半个孔更好的技术，这很难做到。

自然，这不是我们看到的第一个[小 Arduino](http://hackaday.com/2012/08/13/teensy-tiny-arduino-board-with-an-attiny85/) 。如果你是 ARM 粉丝，也有一些[的小卡片](http://hackaday.com/2016/02/18/tiny-usb-morse-code-beacon/)，虽然没有 DIL-Duino 那么小。
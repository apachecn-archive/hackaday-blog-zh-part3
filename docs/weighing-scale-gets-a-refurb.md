# 父亲和儿子修理秤

> 原文：<https://hackaday.com/2016/01/16/weighing-scale-gets-a-refurb/>

当你能和你的父亲一起修理房子周围的东西时，那真是太棒了。在父亲的帮助下，伊利亚·吉查斯基尔(Ilias Giechaskiel)彻底翻新了一台坏了的浴室体重秤(T1)，但之前他试图先修好它。电压调节器看起来坏了。直接给电路的其余部分供电似乎不起作用，而且没有一个无源器件看起来可疑。大多数芯片的标记都被刮掉了，而且玉米棒显然也无法更换。

他们没有对 LCD 显示器进行逆向工程，而是决定只保留传感器和开关，并更换其他所有部件。ATtiny85 似乎有足够的 IO 引脚来完成这项工作。但是，以电桥配置连接的应变式称重传感器的信号跨度不够大，无法使用 ATtiny 上的 10 位 ADC 进行测量。相反，他们决定使用[hx 711](https://cdn.sparkfun.com/datasheets/Sensors/ForceFlex/hx711_english.pdf)(PDF)——一款具有可选增益的 24 位 ADC，专门用于电子秤。使用为 HX711 编写的[库允许它轻松地与 Arduino 接口。该显示器采用由](https://github.com/bogde/HX711) [MAX7219](https://datasheets.maximintegrated.com/en/ds/MAX7219-MAX7221.pdf) 驱动的 4 位 7 段显示器。一个稍加修改的 LEDcontrol 库可以很容易地将显示器连接到 ATtiny 上。该电路被组装在原型板上，以便可以插入另一个 Arduino 进行编程。

由于引脚不足，他们不得不想出一个妙招，用 ATtiny 中的一个引脚作为显示驱动器和 ADC 芯片的时钟。实现上电和自动关机功能需要另一个有趣的模拟电路模块。爸爸在原型板上组装电路。事后看来，ATtiny 上 IO 引脚的缺乏限制了他们可以实现的功能，因此两人计划放入一个 Arduino Nano 来改善黑客攻击。如果你被坏了的秤卡住了，他已经准备好了[原理图](https://ilias.giechaskiel.com/posts/arduino_scale/schematics.png) (PNG)和[代码](http://code repository https://github.com/giech/arduino_scale)供你使用。
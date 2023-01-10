# 降压转换器效率

> 原文：<https://hackaday.com/2018/06/02/buck-converter-efficiency/>

当有人花时间构建一些东西，然后使用真正的硬件演示不同的设计选择会产生什么影响时，我们总是很感激。当然，你可以算出数学和做模拟，但有了真正的硬件，它才是有形的。[Julian Ilett]最近发布了两个符合这一描述的视频。他制造了一个降压转换器，并使用不同的配置对其效率进行了测量。

测试设置很简单。他用示波器监控驱动 PWM，并在输入和输出端安装功率表。这使得测量效率变得容易，因为它只是功率输出与输入的比率。你可以看到下面的两个视频。

有趣的是，各种设计选项确实会改变效率，但可能没有你想象的那么大。最终的范围是 72%到 84%——除非你把导致效率为 0%的低端器件去掉，因为没有它电路就无法工作。

如果您希望[重温一下](https://hackaday.com/2016/06/04/how-does-a-buck-converter-work-anyway/)降压转换器的工作原理，即一种将较高输入电压降低至所需电压的直流-DC 转换器，我们最近有一个很好的视频。如果你想要更多的白板和解释，你可能会喜欢同一主题的 [Sparkfun 视频](https://hackaday.com/2015/01/24/a-primer-on-buck-and-boost-converters/)。

 [https://www.youtube.com/embed/ItCc_t6HPSA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ItCc_t6HPSA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/njMm0ntVaCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/njMm0ntVaCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


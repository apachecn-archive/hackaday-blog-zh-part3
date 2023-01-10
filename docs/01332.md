# 皇家 LED 测试仪

> 原文：<https://hackaday.com/2016/01/29/led-tester-royale/>

对于什么都有，喜欢 led 的极客，你送什么？当然是精心设计的 LED 测试仪。[戴夫·库克]的[豪华型号](http://robotroom.com/LED-Tester-Pro-1.html)配备了一个液晶显示屏和两个可调值:所需电流和电源电压。拨入这些，插入你的 LED，里面的微型电子大脑计算出你需要的电阻值。这有多简单？

LED 测试仪可以像恒流电源一样简单，事实上这就是[戴夫]的第一个 LED 测试仪的本质。例如，将 LM317 电路设置为输出 10mA，您就可以安全地测试任何 LED。读取工作电压，将其从电源电压中减去，然后除以所需的电流，即可计算出所需的电阻。只需要几秒钟，但那几秒钟太多了！

新设备通过在组合中添加一个 AVR ATtiny84 来为您计算。微控制器读取恒流源所需的电压，进行上述减法和除法运算，并显示所需的电阻。如此简单。正如他在下面的视频中演示的那样，它具有二极管测试器的双重功能。

这是一个很棒的初学者项目，它介绍了一堆基本概念:读取 ADC、写入 LED 屏幕、构建恒流电路等。最后，你有了一个有用的工具。这将是一个伟大的工具包！

 [https://www.youtube.com/embed/O7f8aU2HzOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O7f8aU2HzOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


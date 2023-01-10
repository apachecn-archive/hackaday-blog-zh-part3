# 新零件日:带可编程逻辑的 ATMegas

> 原文：<https://hackaday.com/2018/03/02/new-part-day-atmegas-with-programmable-logic/>

自从 Microchip 收购 Atmel 后，战场上一片寂静。十字军已经回家了，或者被赶进了海里。伟大的微控制器圣战结束了。

与任何收购一样，两条产品线之间必然会有一些交叉。Atmel 的 AVR 平台和 Microchip 的 PICs 都有其追随者，现在我们开始看到你最喜欢的微控制器中怪异而奇妙的电路和设计的一些交叉，无论那可能是什么。Microchip 的最新产品是 ATMega，它有一个通常在图片中可以找到的特征。这是一个核心独立外设。这是什么？嗯，这有点像芯片中的 CPLD，它将被放在新的 Arduino 板中。

ATMega4809 是一长串 atmega 中最新的一款，拥有你通常所期待的最新 8 位 AVR 的特性。它运行在 20 兆赫，有 48 K 的闪存，6 K 的 SRAM，并在 48 针 QFN 和 TQFP 封装。到目前为止，一切都如你所料。有什么新的热点？它是一个可配置定制逻辑(CCL)形式的核心独立外设，可以将简单的任务卸载到硬件上，而不是在软件中瞎折腾。

那么，你能用可配置的定制逻辑做什么呢？有一个应用笔记。CCL 实际上是一个具有三个输入的查找表。这些输入可以连接到 I/O 引脚，由模拟比较器、定时器、UART、SPI 总线驱动，或者由内部事件驱动。查找表可以配置为三输入逻辑门，该门的输出通向微控制器芯片的其余部分。基本上，它是一点点可编程的粘合逻辑。在应用笔记中，Microchip 提供了一个利用 CCL 实现开关去抖的例子。这是一个足够简单的例子，而且它会起作用，但是这里有大量的机会和可能性。

此外，根据我收到的新闻稿，ATMega4809“已被选为下一代 Arduino 板的板载微控制器”。我们期待着新的硬件，当然还有一些利用这一点点定制可编程逻辑的库。
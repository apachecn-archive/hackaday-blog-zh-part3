# 用 ESP-gdbstub 压扁你的 ESP-8266 bug

> 原文：<https://hackaday.com/2015/12/12/squash-your-esp-8266-bugs-with-esp-gdbstub/>

我们希望我们的建议不会冒犯您，但是即使是我们当中最优秀的人也可能会不时地面临嵌入式代码中的错误。虽然我们非常喜欢通过串行端口进行调试，以及它的高速等价物——翻转 GPIO 引脚——但有时你的错误是如此之深，以至于拥有一个真正的调试器是挖掘它的最佳方式。

[slaff]已经在 ESP-8266 上做了一些很好的 C/C++编程文档工作，主要是使用 Eclipse 和一些 Arduino 库。在他的系列文章的第四部分中，[他介绍了如何为 ESP](https://blog.attachix.com/live-debugging-with-open-source-tools-programming-for-esp8266-part-4/) 使用几个调试器选项。让这一切工作的是来自 Espressif 他们自己的 [ESP-gdbstub](https://github.com/espressif/esp-gdbstub) 代码。gdbstub 看起来很棒——它既可以与标准 SDK 一起工作，也可以与 FreeRTOS 一起工作，因此无论是在操作系统中还是在裸机上，您都可以调试您的 ESP-8266 代码。所有这些只是使用用于编程的标准串行连接。

现在，这可能仍然无助于解决与时间相关的错误。毕竟 ESP-gdbstub 使用的是串口。但是，能够设置断点并交互检查芯片内存中正在发生的事情是无价的，并且在没有额外硬件连接的情况下这样做是明智的。

 [https://www.youtube.com/embed/oVkwiyqHnvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oVkwiyqHnvY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



当轴碰到鳍时，你真的需要提高你的 ESP，最近也有一堆关于 ESP-8266 目标的 [OpenOCD](http://www.esp8266.com/viewtopic.php?f=9&t=1871) 的工作。特别是，[GitHub](https://github.com/sysprogs/esp8266-openocd)上的这个 fork 完全支持断点、中断、看门狗处理和延续。但是对于日常调试来说，很难击败 gdbstub 的简单性。

如果你只是想看看这些调试的喧嚣是关于什么的，看看我们自己的[Mike Szczys]的使用 OCD 来修复他的 snake 代码中的问题的[视频演示。](http://hackaday.com/2012/09/27/beginners-look-at-on-chip-debugging/)
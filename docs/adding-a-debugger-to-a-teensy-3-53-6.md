# 向 Teensy 3.5/3.6 添加调试器

> 原文：<https://hackaday.com/2017/05/01/adding-a-debugger-to-a-teensy-3-53-6/>

Teensy 是一个强大的基于 ARM 的开发板，具有许多功能，可以用 USB 做有趣的事情。像许多开发板一样，它使用一个不太强大的处理器作为接口。Teensy designer [Paul Stoffregen]添加了一个调试头，允许 SWD JTAG 直接访问主芯片，但接口微控制器必须静音才能工作，这样做的代码仍在开发中。

心急的[Erich Styger] [记录了他为增加对 J-Link SWD 协议](https://mcuoneclipse.com/2017/04/29/modifying-the-teensy-3-5-and-3-6-for-arm-swd-debugging/)的支持所做的更改，删除了有问题的恩智浦 Kinetis KL02Z，作为板载接口和引导加载程序，帮助 Arduino IDE 与主芯片 K64F 对话。KL02Z 被移除后，[Erich]填充了调试头，然后将 Segger J-Link 连接到电路板，并使用 Eclipse、GDB 和标准 SWD 调试工具对其进行了测试。

最终结果是，Cortex M4F 板可以使用标准工具，价格仅为 Kinetis 开发板的三分之一。[Paul Stoffregen]证实[调试功能将很快添加到引导加载程序代码中](https://forum.pjrc.com/threads/42728-Debugging-strategies)，但在此之前，硬件黑客是在平台上进行调试的一种有效方法，尽管很残酷。

感兴趣的人可以获得更多关于 JTAG 界面的信息。如果你不喜欢 Teensy，你可以考虑基于 STM32 的[开发板](http://hackaday.com/2017/03/30/the-2-32-bit-arduino-with-debugging/)。

 [https://www.youtube.com/embed/SWO4CgkVlGI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SWO4CgkVlGI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


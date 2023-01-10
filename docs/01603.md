# Linux 物联网

> 原文：<https://hackaday.com/2016/02/25/the-internet-of-linux-things/>

Linux 基金会是一个非盈利组织，赞助 Linus Torvalds 的工作。支持公司包括惠普、IBM、英特尔和许多其他大公司。该基金会主持了几个与 Linux 相关的项目。本月，他们发布了针对物联网的 RTOS 产品[泽法。](http://www.linuxfoundation.org/news-media/announcements/2016/02/linux-foundation-announces-project-build-real-time-operating-system)

该项目强调模块化、安全性和尽可能小的占地面积。初始支持包括:

*   Arduino 101
*   arduino 号
*   英特尔伽利略第二代
*   恩智浦 FRDM-K64F 自由

该项目(托管在自己的网站上)有内核和文档的下载。与“普通的”Linux 内核不同，泽法用您的代码构建内核，以创建一个运行在单一共享地址空间中的整体映像。构建系统允许您选择您想要的特性，并排除那些您不需要的特性。您还可以自定义所包含内容的资源利用率，并在编译时定义资源。

默认情况下，有最小的运行时错误检查来保持可执行文件精简。但是，有一个可选的错误检查基础结构，您可以将其包含在调试中。

该 API 包含了您期望从 RTOS 得到的东西，比如纤程(轻量级非抢占式线程)、任务(抢占式调度)、信号量、互斥体和大量消息传递原语。此外，还有针对 PWM、UARTs、通用 I/O 等的常见 I/O 调用。API 在所有平台上都是一致的。

你可以在下面的视频中找到更多关于泽法的信息。当然，我们以前见过 [RTOS 系统](http://hackaday.com/2015/04/17/energia-multitasking-uses-rtos-on-msp432/)。甚至还有一些为[机器人](http://hackaday.com/2014/01/29/the-robot-operating-system-ros-101/)准备的。然而，对于需要 RTOS 的复杂项目来说，拥有一个可以针对像 Arduino Due 和 Freedom 板这样的小板的 Linux 传统 RTOS 可能是一个真正的游戏规则改变者。

 [https://www.youtube.com/embed/JEpY_ETJ_jE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JEpY_ETJ_jE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


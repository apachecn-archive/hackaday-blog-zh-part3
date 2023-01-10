# 忘记特洛伊。试试 HelenOS

> 原文：<https://hackaday.com/2017/08/20/forget-troy-try-helenos/>

尽管看起来有很多操作系统可供选择，但是如果你开始计算内核，而不是发行版，这个数字就变小了。当然，Windows 显然是一个操作系统家族，在类 Unix 方面，有 Linux 和 BSD。但是许多其他操作系统——Ubuntu、Fedora、Raspian——它们都是从一些普通操作系统衍生而来的。不过，也有一些例外，其中之一就是 HelenOS。开源操作系统可以在许多平台上运行，包括 PC、Raspberry PIs、Beaglebones 等等。

虽然这个操作系统不是新的，但它正在获得更多的功能，现在是 0.7 版本。你可以在下面看到一段关于一些新功能的视频。

根据该项目的网站:

> HelenOS 是一个可移植的基于微内核的多服务器操作系统，从头开始设计和实现。它将文件系统、网络、设备驱动程序和图形用户界面等关键操作系统功能分解为一组细粒度的用户空间组件，这些组件通过消息传递相互交互。一个组件的故障或崩溃不会直接伤害其他组件。因此，HelenOS 是灵活的、模块化的、可扩展的、容错的和易于理解的。

开发团队在其 FAQ 中提到，代码对于生产使用来说可能不够稳定，但是他们认为它已经接近于实际使用了。可用的 API 不是对等的 Linux API 的副本，后者给操作系统带来了更多的灵活性，但却增加了移植现有代码的难度。有一份文件[概述了差异](http://www.helenos.org/wiki/DiffFromUnix)。

尽管这个操作系统没有使用 Linux API，但它并不像我们见过的其他一些操作系统那样遥远。有更好的主意吗？你可以学习[在树莓 Pi](http://hackaday.com/2012/09/02/operating-systems-development-with-the-raspberry-pi/) 上投入操作系统开发，然后自己动手做。

 <https://mirrors.dotsrc.org/fosdem/2017/AW1.125/microkernel_helenos_year_of_the_fire_monkey.mp4?_=1>

[https://mirrors.dotsrc.org/fosdem/2017/AW1.125/microkernel_helenos_year_of_the_fire_monkey.mp4](https://mirrors.dotsrc.org/fosdem/2017/AW1.125/microkernel_helenos_year_of_the_fire_monkey.mp4)
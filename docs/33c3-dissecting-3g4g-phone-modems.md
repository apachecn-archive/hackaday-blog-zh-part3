# 33C3:剖析 3G/4G 电话调制解调器

> 原文：<https://hackaday.com/2017/02/20/33c3-dissecting-3g4g-phone-modems/>

[LaForge]和[Holger]已经在手机方面进行了相当长一段时间的研究，这导致他们在 OpenMoko 开发开放式手机，并开发 OsmocomBB GSM SDR 软件。现在，他们将目光转向 3G 和 4G 调制解调器，主要是因为他们想在自己的设备中使用它们，但也想让更广泛的黑客社区能够使用它们。在第 33 届混沌通信大会(33C3)的这次演讲中，他们讨论了他们在让现代智能手机最黑暗的部分为我们其他人所用方面的进展。

这个演讲不是关于现代手机调制解调器的即插即用，而是关于重新编程。他们选择了高通芯片组，因为它有一个有用的 DIAG 协议，特别是选择了 iPhone5 中使用的 Quectel EC20 调制解调器，因为它可以轻松获得 DIAG 流。

我们的故事从制造商的固件升级开始。他们解压文件，惊喜地发现它实际上运行的是 Linux，没有文档记录，也没有可用的源代码。现在，[LaForge]恰好是 gpl-violations.org 的创始人，他对从使用 Linux 的供应商那里获取代码而不遵守条款和条件略知一二。法律故事漫长而复杂，仍在继续，但他们从 Quectel 那里获得了大量代码，看起来他们正在努力弥补。

另一方面，高通提供 Linux 内核源代码，即使没有文档。(这是 Quectel 的代码所基于的来源。)[LaForge]接手了记录它的任务，然后为它开发一些工具——正在进行的事情比我们所能涵盖的还要多。如果你准备好深入研究，他们工作的所有[成果都可以在维基网站](https://osmocom.org/projects/quectel-modems)上找到。

就目前的情况来看，[Holger]和[LaForge]已经记录了很多运行在 EC20 电话调制解调器内部的 Linux 系统，所以开发的时机已经成熟。他们建立了一个工具链，这样你就可以编译和闪存内核到调制解调器，还有一个 Android 调试桥(adb)根外壳，所以你基本上可以做任何事情。这不是 Arduinery——在你将这些模块直接用于自己的项目之前，还有很多真正的工程工作要做——但直到现在，4G 和 LTE 电话调制解调器对黑客社区来说一直是一个完全不透明的黑匣子。至少现在我们有了一个立足点。

[https://media.ccc.de/v/33c3-8151-dissecting_modern_3g_4g_cellular_modems/oembed](https://media.ccc.de/v/33c3-8151-dissecting_modern_3g_4g_cellular_modems/oembed)
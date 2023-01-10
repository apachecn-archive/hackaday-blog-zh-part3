# 英特尔的管理引擎坏了吗？

> 原文：<https://hackaday.com/2017/11/17/is-intels-management-engine-broken-yet/>

就在六个月前，我们的布莱恩·本考夫在类似的标题中提出了同样的问题。当时，答案是否定的。或者说是否定的。有些漏洞是存在的，但有一些先决条件，限制了在英特尔管理引擎(ime)中发现的缺陷的影响。但 2017 年对蓝队来说是不可原谅的一年，因为在这一年里，几乎每个计算领域都发现了许多严重的错误。来自积极技术[的研究人员报告说，他们发现了一个缺陷，允许他们在运行 IME 的计算机上执行未签名的代码](https://thenextweb.com/security/2017/11/09/researchers-find-almost-every-computer-intel-skylake-cpu-can-owned-via-usb/)。蛋糕上的樱桃是，他们能够通过一个 USB 端口作为 JTAG 端口。这是否意味着僵尸末日即将来临？

在 2015 年发布的 Skylake CPU 系列之前，JTAG 接口只能通过将一种特殊设备连接到电脑机箱内主板上的 ITP-XDP 端口来访问。从 Skylake CPU 开始，英特尔取代了 ITP-XDP 接口，并允许开发人员和工程师通过通用 USB 3.0 端口访问调试实用程序，可以通过一种称为直接连接接口(DCI)的新技术从设备外部访问。基本上，DCI 通过 USB 3.0 提供对 CPU/PCH JTAG 的访问。因此，研究人员设法通过 USB DCI 调试 IME 处理器本身，这非常棒，但 USB DCI 在默认情况下是关闭的，就像一名研究人员所说的那样，这对普通用户来说是个好消息。所以现在还不要太担心。

我们推荐[【板凳队员】关于 IME](https://hackaday.com/2017/05/02/is-intels-management-engine-broken/) 的精彩文章，以防你对它有疑问。简而言之，IME 是一个完全独立的处理器，只要连接电源线，即使电脑关闭，它也可以控制网络和硬件。虽然是独立的，但是被烤进主处理器芯片(Intel inside Intel inside？)所以没有办法删除它，但是[有办法禁用它](https://hackaday.com/2016/11/28/neutralizing-intels-management-engine/)，至少在某些处理器中。由于 IME 在不同的 CPU 上执行代码，[显然运行 MINIX](https://hackaday.com/2017/11/11/nearly-all-your-computers-run-minix/) ，它的网络操作绕过任何安装的操作系统，对主机完全不可见，还有其他很酷的“功能”。这太酷了，以至于欧洲足联实际上指责 IME 是一个后门。

在其他新闻中，[贝特里奇的头条新闻定律](https://en.wikipedia.org/wiki/Betteridge's_law_of_headlines)似乎仍未被打破。
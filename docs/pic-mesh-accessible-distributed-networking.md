# PIC 网格，可访问的分布式网络

> 原文：<https://hackaday.com/2016/12/17/pic-mesh-accessible-distributed-networking/>

对于我们大多数人来说，无线网络已经被简化为一个组件。我们安装了一个设备，可能是一个 ESP8266 模块或类似的东西，就像变魔术一样，一个网络存在了。底层技术已经被抽象到设备的固件中，我们从来不会直接碰到。这不是一件坏事，因为使用无线通信而不必担心它的机制给了我们继续工作的自由。

然而，偶尔观察一下真实无线网络的运行是很有趣的，[亚历克斯·王]、[布莱恩·克拉克]和[拉格哈瓦·库马尔]给了我们一个项目，让我们有机会做到这一点。他们的 PIC Mesh 大学项目是[一个使用 2.4GHz NRF24L01 收发器模块和 PIC32 微控制器](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/bac239_aw528_rk534/bac239_aw528_rk534/bac239_aw528_rk534/index.html)的分布式无线网状网络。他们将它配置为在应用层使用家庭自动化系统进行演示，但是它也可以应用于许多其他应用。

这个项目的真正价值在于它的全面但易于阅读的文章，就像你从大学项目中所期望的那样。上面链接的首页概述了网格如何工作，但也有页面带我们浏览[硬件](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/bac239_aw528_rk534/bac239_aw528_rk534/bac239_aw528_rk534/hardware.html)、[网络软件层](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/bac239_aw528_rk534/bac239_aw528_rk534/bac239_aw528_rk534/mesh_software.html)和[家庭自动化应用层](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/bac239_aw528_rk534/bac239_aw528_rk534/bac239_aw528_rk534/auto_software.html)。如果您曾经想了解一个简单的网状网络系统，这是一个很好的起点。

这些年来，我们已经介绍了相当多的网状网络，但遗憾的是，我们只能将您与其中的一些联系起来。我们已经有了使用 Raspberry Pi 的网状网络(T1)、拜占庭项目(T2)的“僵尸启示录(T3)专用无线网状网络(ad-hoc wireless mesh networking)和用于测试目的的 1000 节点 Xbee 网络(T5)。
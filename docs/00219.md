# Hackaday 奖半决赛:数控成为挑选和放置

> 原文：<https://hackaday.com/2015/09/28/hackaday-prize-semifinalist-cnc-becomes-pick-and-place/>

在 80 年代和 90 年代，制造专业质量的 PCB 是一个昂贵的提议。即使你买得起最新主板的几块面板，在上面安装组件也是一个昂贵的过程。现在，我们有廉价的印刷电路板、基于烤面包机的焊接炉和其他一切东西来制造廉价的成品电路板*，除了用于取放机的*。ProtoVoltaics 的[hack aday 奖半决赛参赛作品就是这个问题的答案](https://hackaday.io/project/5200-pick-and-place-machine)。他们正在把一台便宜的现成数控机床改造成一台取放机床，这对任何黑客空间或设备齐全的车库车间来说都是一个受欢迎的补充。

ProtoVoltaics 公司没有制造他们自己的直角坐标机器人，而是围绕一台 [X-Carve](https://www.inventables.com/technologies/x-carve) 制造他们的抓放机器人，这是一台造价约为 1000 美元的数控刳刨机。在这个平台上，ProtoVoltaics 增加了所有的机制和智能，将几个网络摄像头和一台 CNC 机器变成一台合适的拾取和放置机器。

在 X-Carve 的新增功能中，有一个新的工具头，它能够从卷轴中吸取零件，并将其吐在一滴焊膏上。网络摄像头由包含 CUDA 加速计算机视觉的软件监控。

当然，没有进料器，取放机就没什么用了，为此，ProtoVoltaics 开发了自己的开源进料器。将所有这些元素放在一起，你就拥有了一台每小时能够放置多达 1000 个元件的机器；对于任何小规模生产来说都绰绰有余，对于一些相当大规模的实际产品来说也足够了。

你可以看看下面这个项目的一些视频。

#### 2015 年[黑客日奖](http://hackaday.io/prize)由以下机构赞助:

[![](img/8e6c49d55ea91b307d7d191b75ab18c8.png)](http://hackaday.io/atmel)[![](img/6b53a13e67e0346985e237ef126c1bcc.png)](http://hackaday.io/freescale)[![](img/3fe105965ef22414d89f71032d9babee.png)](http://hackaday.io/microchip)[![](img/ebcbe4e97993de26ebcf849e70523a14.png)](http://hackaday.io/mouser)[![](img/15f4f8aaed16b020832d8be6282e47f5.png)](http://hackaday.io/ti)

 [https://www.youtube.com/embed/Ny99KzsySHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ny99KzsySHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/uNBV_dabrDA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uNBV_dabrDA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


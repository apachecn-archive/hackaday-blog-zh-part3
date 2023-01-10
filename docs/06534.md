# 控制你的廉价激光切割机

> 原文：<https://hackaday.com/2017/07/19/take-control-of-your-cheap-laser-cutter/>

来自中国的相对便宜的 K40 激光切割机/雕刻机给大众带来了激光切割，但它们也不是没有缺点。当然，它们只对最轻的切割任务足够强大，但最重要的是，它们的捆绑软件不够灵活，令人失望。如果你的工作室或黑客空间有一台这样的机器在角落里萎靡不振，那么[一款新软件的发布，来自【Scorch】的 K40 Whisperer】，是一个有趣且受欢迎的发展。](http://www.scorchworks.com/Blog/k40-whisperer-k40-cheap-chinese-laser-control-software/)

他告诉我们，理解 K40 协议所需的逆向工程过程并不简单，因为它不使用方便的十进制数字来发布命令。一个电子表格被用来整理数据包，找出重复的模式来分析内部运作。功能方面，该软件读取 SVG 和 DXF 文件，并可以按颜色分割 SVG。它有一个用于渲染灰度的半色调算法，并首先从每个形状的内部进行切割，以避免作品从材料中掉出。目前，它可以与 M2 的 Nano 控制器主板兼容，[可以从 Windows 下载](http://www.scorchworks.com/K40whisperer/k40whisperer.html)，尽管它也可以为 Linux 发行版或 MacOS 编译，他要求用户在尽可能多的机器上测试它，以确保与其他主板的兼容性。

他发布了一个 K40 耳语者的视频，你可以在下面看到。

 [https://www.youtube.com/embed/PEUJQFAEDcE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PEUJQFAEDcE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这不是改进你的 K40 的唯一方法，[你可以放入一个新的控制器](http://hackaday.com/2017/06/10/drop-in-controller-for-ebay-k40-laser-engraver-gets-results/)，或者甚至[增加它的床的尺寸](http://hackaday.com/2017/04/24/laser-surgery-expanding-the-bed-of-a-cheap-chinese-laser-cutter/)。
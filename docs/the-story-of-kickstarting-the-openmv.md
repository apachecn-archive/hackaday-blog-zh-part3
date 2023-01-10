# 启动 OpenMV 的故事

> 原文：<https://hackaday.com/2016/12/29/the-story-of-kickstarting-the-openmv/>

机器人是现在最流行的东西，计算机视觉是一个热门话题，微控制器从未如此之快。这些事实不可阻挡地导致了 OpenMV 的出现，这是一个嵌入式计算机视觉模块，自称是“机器视觉的 Arduino”。

最初的 OpenMV 是第一届 Hackaday 奖的参赛作品，从那以后这个项目取得了很大的成功。有大量的追随者和用户，这个项目甚至有一个成功的 Kickstarter。最后一点信息相当有争议——虽然 Kickstarter 确实达到了最低融资水平，但将这款非常酷的产品推向市场存在很多问题。供应商和社区管理的问题是最大的问题，但 OpenMV 背后的团队最终成功了。

在 [2016 黑客日超级大会](https://hackaday.io/superconference/)上，OpenMV 的项目负责人之一夸贝纳·阿杰曼讲述了将 OpenMV 推向市场的故事:

 [https://www.youtube.com/embed/JEFcKylxfIw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JEFcKylxfIw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



OpenMV 是一个计算机视觉模块，非常便宜，也非常简单。这个模块实际上只有两个主要部分:一个功能强大的微控制器和一个能够捕捉原生 JPEG 格式图像的相机模块。OpenMV 价格低廉的原因是因为相机模块本身价格低廉——它是一种大约有十年历史的传统图像传感器，但如果你在微控制器上进行计算机视觉，你真的不需要很多百万像素。

那些旧的相机传感器回来咬 OpenMV 项目。显然，当你使用 10 年前的 BGA 部件时，有时球会变坏。OpenMV 项目见证了他们 80%的图像传感器在组装过程中出现故障，甚至被评为[本周黑客故障](http://hackaday.com/2015/11/05/fail-of-the-week-openmv-kickstarter-project-hits-manufacturing-snag/)。

为了弄清这个问题，Kwabena 给这些图像传感器的制造商打了电话，发现了这个问题。这些图像传感器从未在公开市场上出售，仅出售给原始设备制造商。这些图像传感器进入 OpenMV 供应链的最有可能的方式是，它们原本是用于手机的，但它们要么被拆焊并放入模块中，要么只是作为未使用的库存被卸载到全球速卖通。

这个问题的解决方案是什么？不幸的是，另一个制造运行与一个新的相机模块的成本约 18000 美元。这是一个成功，OpenMV 社区得到了他们新的、升级的计算机视觉模块。

现在，OpenMV 摄像机已经在野外使用，并且一个社区正在他们周围成长，这个计算机视觉模块的创造者决定对他们的硬件进行一次新的迭代。新的 OpenMV 使用了更快的处理器，内存更大，价格比原来的更低。

在 Hackaday，我们非常熟悉生产过程中可能出现的问题。我们已经看到几十个 Kickstarters 因为运气不好或计划不周而失败。OpenMV 遇到的麻烦是无法计划的，要解决这些问题需要运气或者大量的工作。他们做到了，结果是围绕他们创造的硬件建立了一个繁荣的社区。这太棒了，也是我们在 2016 年 Hackaday 超级大会上听到的最好的硬件成功故事之一。
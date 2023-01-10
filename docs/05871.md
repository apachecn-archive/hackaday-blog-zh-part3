# 悬浮滑板的开源固件

> 原文：<https://hackaday.com/2017/05/07/open-source-firmware-for-hoverboards/>

2015 年是两年前，令许多人惊讶的是，我们当时实际上已经有了悬浮滑板。当然，这些不是*回到未来*式的悬浮滑板；它们是蹩脚的两轮平衡滑板车，电池发生了几次爆炸，最终被一些航空公司禁止在国内航班上使用。*但是哦，孩子，这些东西有一些有趣的藤蔓*。

当世界上的其他人从悬浮滑板中走出来的时候，[Casainho]一直在为这些有趣的电子设备和电机开源固件。现在，他的工作已经接近尾声，他有了电动独轮车和悬浮滑板的新固件。

在过去的五年里，流行而廉价的电动独轮车和悬浮滑板从伟大的阿里巴巴游过太平洋，它们都是基于一个单一的廉价控制板。该控制器板围绕 STM32F1038T6 微控制器构建，能够控制一对三相无刷电机。拆除开始于[电动独轮车论坛](http://forum.electricunicycle.org/topic/1109-firmware/?page=41#comment-90781)，并在 GitHub 回购中完整记录[。](https://github.com/EGG-electric-unicycle/documentation/wiki/MicroWorks-30B4-30kmh-controller-board-with-bluetooth)

开源固件是[现在大部分完成](https://github.com/EGG-electric-unicycle/firmware-gen2_boards/tree/modifiedFOC-motorMicroWorks30kmh)，虽然必要的自平衡功能不起作用。我们认为这没关系。有了这个新的固件，这些电动独轮车有了疯狂的扭矩，可以成为一些非常酷的构建的基础。你可以看看下面这个扭矩的视频。

如果两个轮子看起来太安全，用 3D 打印的独轮车转换成悬浮滑板来锻炼你内心的勇气。

 [https://www.youtube.com/embed/2nDZW4-uVys?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2nDZW4-uVys?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


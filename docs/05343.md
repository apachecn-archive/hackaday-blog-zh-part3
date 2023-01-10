# 动画相框需要每月充电一次

> 原文：<https://hackaday.com/2017/03/19/animated-picture-frame-needs-charging-once-per-month/>

[Kyle Stewart-Frantz]看了一眼一张山间小溪的黑白照片，觉得太无聊了。如果[水在流动](https://medium.com/@kylesf/my-experience-in-creating-the-worlds-first-low-power-animated-picture-frame-ee24877a4b46#.jpzx3vo9h)会有多凉爽！像任何一个在 2N2222s 中与其体重相当的优秀黑客一样，[Kyle]着手将他的想法变成现实。在发现了一些[昂贵的选项](https://www.visionect.com/product/visionect-development-kit-32-grayscale/)后，他找到了一个带有![](img/ab19d963c4b6a684b7d52904d58eb971.png)显示屏的 Kindle Paperwhite，它有不错的分辨率和 16 级灰度。但是 16 个关卡足以制作出赏心悦目的动画吗？

在偶然发现一个致力于黑客 Kindles 的社区后，[凯尔]开始工作。使用一个名为 [eips](https://wiki.mobileread.com/wiki/Eips) 的定制亚马逊命令，他能够访问显示器的存储位置并在其上绘制图像。下一个技巧是编写多次调用该命令的脚本，以产生类似 GIF 的动画效果。这个…效果不太好。然后，他从[GeekMaster]找到了一些代码(感谢您的提示！)在 Kindle 上运行了一个专门的视频播放器，它使用了一种叫做[的东西来控制抖动](https://en.wikipedia.org/wiki/Ordered_dithering)。经过几次调整后，他让一切正常工作，最终结果看起来像是直接来自哈利波特的世界。

动画相框可以在充电之间运行三到四周。这是一个很好的礼物，放在你的办公室会很好看。如果你做了一个，一定要先把头骨和扳手放上去，然后告诉我们！

[https://player.vimeo.com/video/208188320](https://player.vimeo.com/video/208188320)
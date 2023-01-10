# 在 OpenCV 中创建视频轨迹

> 原文：<https://hackaday.com/2015/10/03/creating-video-trails-in-opencv/>

视频痕迹效果并不新鲜:它首次用于音乐视频，如 1978 年杰克逊五兄弟乐队的“归咎于布吉”。现在，[Antonio Ospite]整理了一篇很好的文章，展示了使用 OpenCV 在直播视频中创建这种效果的基础知识。他为此使用了开源视频处理包 [OpenCV](http://opencv.org/) ，用一个简短的脚本创造了这个效果。它可以以多种方式运行，创建视频尾迹效果，或“追赶”尾迹(尾迹反转为最终帧)。

这提供了一个有趣的例子，说明这些视频效果是如何变得如此容易创建的。杰克逊 5 号的视频是用 T2 的 Scanimate 和 Quantel 的颜料盒系统制作的，这个系统和壁橱一样大，花费了几十万美元。现在，你可以用免费软件和便宜的电脑创造这些效果。现在你只需要弄清楚在我们的现代世界中，有了这种倒退效果，什么看起来很棒。

 [https://www.youtube.com/embed/X3oRozxt2O4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=75&wmode=transparent](https://www.youtube.com/embed/X3oRozxt2O4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=75&wmode=transparent)



 [https://www.youtube.com/embed/mkBS4zUjJZo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mkBS4zUjJZo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


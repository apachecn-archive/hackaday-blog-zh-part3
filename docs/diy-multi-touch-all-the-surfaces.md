# DIY 多重触摸所有表面

> 原文：<https://hackaday.com/2017/11/04/diy-multi-touch-all-the-surfaces/>

曾经想要建立一个触摸表或其他触摸输入项目，但陷入了计算“触摸”的一部分？[Jean Perardel]在 IO 上用他的[多点触摸框架支持你，使任何表面都可以触摸反应](https://hackaday.io/project/27155-magic-frame-turn-everything-into-a-touch-area)。在[Jean]的例子中，这个表面最终是一个桌子里面的电视。

当然，说表面本身变得可以触摸反应有点用词不当。这里真正发生的是[Jean]正在使用光三角测量来检测阴影并确定投射阴影的物体的坐标。许多条形码扫描仪和消费级文档扫描仪使用接触式图像传感器(CIS)来检测 IR LEDs 路径上的物体。它们是高等级扫描仪中 CCD 的低功耗、低分辨率替代品。

正如[Jean]在下面的视频中解释的那样，在面向任何一种传感器阵列的单个红外 LED 的路径上放置一个物体，都会阻挡光线到达传感器。继续添加 led，它们的发射角度将开始重叠，从而提高检测精度。[Jean]逆向工程了几个不同类型的扫描仪，直到他找到一个合适的。他最终发明了 CIS，在 20 厘米(7.87 英寸)的空间内排列了 2700 个光传感器。

[Jean]设计了一个 3D 打印框架，可容纳 96 个红外发光二极管，三个一组。青少年打开 led，检测触摸事件，计算位置，并将这些坐标发送到 Pi 以显示在屏幕上。他最终使用了无线技术，然后建造了一个漂亮的触摸桌子来放置一台 32 英寸的电视。

这不是构建多点触控表的唯一方法，也不是最简单的方法。[这里有一个使用手指按压来散射光的](https://hackaday.com/2014/01/01/easy-multi-touch-table/)和[一个基于工业强度投影的桌子，它是几年前开源的](https://hackaday.com/2013/09/29/50-multitouch-table-is-expensive-indestructable/)。

 [https://www.youtube.com/embed/2aOYc_GKTHQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2aOYc_GKTHQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


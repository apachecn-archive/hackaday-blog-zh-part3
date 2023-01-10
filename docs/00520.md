# Wii-Motified 激光切割机重新聚焦轮廓切割

> 原文：<https://hackaday.com/2015/11/01/wii-motified-laser-cutter-refocuses-for-contoured-cutting/>

还在 2D 用激光切割你所有的零件吗？不是那边的人[只添加鲨鱼]。通过几行代码和一个完整的 Wii-Mote，他们已经设法[装配他们的激光切割机，根据材料的高度动态地重新聚焦](http://www.justaddsharks.co.uk/blogs/2015-10-29/continuous-autofocus-laser-cutter-hack)。

通过将 Wii-Mote 放置在已知的固定距离和角度以及聚焦光束的视线范围内，黑客攻击被干净利落地执行。幸运的是，Wii-Mote 的图像传感器已经完成了图像处理，它只需返回视图中四个最亮红外点的(x，y)坐标。当光束在材料上移动时，点在相机的视野中上下移动，在切割时触发激光的重新聚焦。考虑到 z 轴工作台需要根据轮廓进行重新调整，[只需添加鲨鱼]的工作人员已经降低了切割速度。最后，值得注意的是，Wii-Mote 的设计是为了检测红外发光二极管，而不是 10600 纳米的激光束，但我们怀疑 Wii-Mote 接收的是荧光材料本身产生的颜色，而不是光束。然而，结果是完全相同的-动态重新聚焦激光！

现在[Glowforge]已经发布了一款用立体相机实现的[连续重聚焦激光切割机](http://glowforge.com/tech-specs/)，很高兴看到社区跟随他们的脚步进行 DIY 努力。休息后查看整个系统的运行情况！

 [https://www.youtube.com/embed/TvP1nIesntg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TvP1nIesntg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


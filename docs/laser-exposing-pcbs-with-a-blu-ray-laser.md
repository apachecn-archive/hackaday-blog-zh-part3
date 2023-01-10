# 用蓝光激光器对多氯联苯进行激光曝光

> 原文：<https://hackaday.com/2017/07/14/laser-exposing-pcbs-with-a-blu-ray-laser/>

对于我们这些几十年前就开始接触 PCB 制作并分享永久记号笔和皱纹纸胶带美好回忆的人来说，今天 PCB 艺术家可用的一系列技术看起来简直是不可思议的。对许多读者来说，调色剂转印和过氧化物蚀刻剂混合物可能看起来很普通，但即使是它们也比过去的前辈领先很多。

抗蚀涂层的照相曝光传统上是用紫外灯透过一张醋酸胶片进行的，但没有理由认为这是唯一的方法。有很多项目使用激光或 led 将 PCB 设计绘制到涂层上作为光栅，[来自[Terje Io]的一个很好的例子](https://www.youtube.com/watch?v=TIDV1zXWXNY)使用蓝光激光二极管，是休息时间下方视频的主题。

二极管安装在一个带有 THK KR33 线性致动器的台架上，他告诉我们，由于反冲，该致动器不适合他的数控铣床。这在 100 毫米 x 160 毫米的曝光面积上提供了声称的 1200 dpi 分辨率。GitHub 库中提供了软件[，通过 PDF 打印机导出 PNG 图像。由于它有一个紫外激光器，它可以用于第二次通过处理紫外线反应阻焊膜。([Terje]作弊，用单独的数控铣床钻出来的孔。)结果看起来很棒。](https://github.com/terjeio)

 [https://www.youtube.com/embed/TIDV1zXWXNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TIDV1zXWXNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



激光 PCB 曝光者以前曾在这里展示过，例如[这个由比格犬骨驱动的例子](http://hackaday.com/2017/06/15/laser-pcbs-with-ldgraphy/)，这个由废弃 CD 驱动器制成的，或者这个[重新利用激光打印机的旋转镜单元](http://hackaday.com/2012/08/09/exposing-pcbs-with-a-home-made-laser-printer/)。我们确信这不会是我们带给你的最后一个。
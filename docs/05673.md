# 光致变色鸡蛋:不是早餐

> 原文：<https://hackaday.com/2017/04/18/photochromic-eggs-not-for-breakfast/>

光致变色涂料非常漂亮——在合适波长的光照射下，它会改变颜色。这给了它各种各样的临时显示器的应用。[【Jiri Zemanek】决定在鸡蛋上涂上光致变色涂料，在激光的帮助下，用它来创造频闪图案。](http://aa4cc.dce.fel.cvut.cz/content/eggstatic-2-how-decorate-easter-eggs-laser-and-photochromic-paint)

鸡蛋的图案是在 MATLAB 中生成的。Discovery STM32 板充当控制器，负责激光扫描仪和旋转鸡蛋的步进电机。光电晶体管用于在鸡蛋旋转时同步激光和鸡蛋的位置。

这个项目中使用的光致变色涂料是由紫外光激活的。为了给油漆提供能量，[Jiri]从蓝光播放器中获取了一束紫色激光，将其安装到激光打印机的扫描组件上。激光不是在成像鼓上扫描，而是在旋转的鸡蛋上垂直扫描。然后可以在鸡蛋上绘制图案，随着时间的推移，图案会随着颜料释放储存的能量而褪色。

[Jiri]利用这一点，在鸡蛋上写下各种图案，然后以类似于[光镜](https://en.wikipedia.org/wiki/Zoetrope)的方式制作动画——当在闪光灯下可视化时，图案看起来会移动。还有一些复活节的节日信息，这使得彩蛋更适合作为广告牌。

如果你喜欢在鸡蛋上画画的想法，但对它们不均匀的几何形状感到不快，那就试试这个[鸡蛋机器人](https://hackaday.com/2010/03/30/cnc-egg-decorating/)。休息下的视频。

 [https://www.youtube.com/embed/rIgpqlrj-G0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rIgpqlrj-G0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


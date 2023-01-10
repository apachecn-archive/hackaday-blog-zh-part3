# 偏振 3D 扫描仪提供惊人的结果

> 原文：<https://hackaday.com/2015/12/23/polarizing-3d-scanner-gives-amazing-results/>

如果你能把 Kinect 这样的廉价 3D 传感器的效率提高三个数量级，会怎么样？当然，Kinect 很棒，但它的分辨率有限。为了增加这一点，麻省理工学院的研究人员正在使用[偏振测量来推断 3D 形式](http://news.mit.edu/2015/algorithms-boost-3-d-imaging-resolution-1000-times-1201)。

[菲涅耳方程](https://en.wikipedia.org/wiki/Fresnel_equations)描述了物体的形状如何改变反射光偏振，研究人员使用接收到的偏振来推断形状。偏振传感器只不过是一个 DSLR 相机和一个偏振滤光器，扫描分辨率低至 300 微米。

菲涅耳方程的问题是存在模糊性，因此单次偏振测量无法唯一识别形状，这里的新颖工作是使用来自 Kinect 等深度传感器的信息从备选方案中进行选择。

这种处理还不是实时的，尽管该团队认为他们可以轻松实现 30Hz 的扫描。除了明显的 3D 打印应用，该团队希望他们的技术偏振 3D 也将对自动驾驶汽车和机器人产生影响。

在过去几年的中，我们已经看到了大量的 [Kinect 扫描仪](http://hackaday.com/2012/09/16/a-portable-wifi-enabled-kinect/)。然而，偏振技术看起来很容易实现，并提供了大幅提高分辨率的承诺。
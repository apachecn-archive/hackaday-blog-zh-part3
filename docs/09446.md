# 史密斯图表时代的标志

> 原文：<https://hackaday.com/2018/05/13/sign-of-the-smith-chart-times/>

史密斯圆图是分析复阻抗的主要工具。[w2aw]指出，许多便宜的测试设备，如 MFJ-259B，给你复数读数，但不能提供复数虚部的符号。这使得在史密斯图上绘制结果或进行其他分析变得困难。正如你所料，他[为你](https://www.youtube.com/watch?v=_Dlw_XheKl0)准备了一个解决方案，你可以在下面的视频中看到。

常见的方法是稍微提高频率。在一个简单的例子中，你会期望虚部——电抗——对于容性阻抗下降，对于感性阻抗上升。不幸的是，这并不适用于许多常见情况，包括当您通过传输线进行测量时，这可能是大多数人使用这种类型的测试设备所做的事情。

奇怪的是，获得正确符号的方法是使用史密斯圆图本身。步骤很简单:

1.  在 3 个不同的频率下进行测量
2.  假设电抗为正，在史密斯图上画出 3 个测量值；然后假设为负，再次绘制它们；你将总共得到 6 分
3.  用从最低频率到最高频率的曲线连接正点集；对负集重复上述步骤

一条曲线顺时针，另一条逆时针。顺时针曲线将位于正确的点上。

听起来很简单，但是看着它实际完成会让它变得更具体。这个例子解决了这个问题，并与一个自动创建史密斯图的自动化工具相一致。

我们总是着迷于史密斯圆图，它本质上是一个画在纸上的模拟计算机。如果你想更直观地了解天线，我们推荐[这款](https://hackaday.com/2016/11/27/start-your-path-to-becoming-an-antenna-guru/)。

 [https://www.youtube.com/embed/_Dlw_XheKl0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_Dlw_XheKl0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


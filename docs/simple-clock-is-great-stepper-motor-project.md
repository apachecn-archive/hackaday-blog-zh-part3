# 简单的时钟是伟大的步进电机项目

> 原文：<https://hackaday.com/2016/07/21/simple-clock-is-great-stepper-motor-project/>

你会认为我们已经在 Hackaday 张贴了所有可能的时钟。事实证明我们没有。但是我们已经看够了，我们已经开始在脑海中对时钟进行分类。有力求精确到每一微秒的精确时钟，有以最独特的机制为目标的 bizzaro 时钟，还有“hello world”时钟，它对建筑材料做了很好的介绍。

今天，我们正在看一个[漂亮的“你好，世界”时钟](http://www.instructables.com/id/A-Weird-Arduino-Powered-Clock/)。[每个人的电子产品]的构建使用步进电机和一个相对于固定指针旋转的大标签轮。滚动轮子，时间就变了。它看起来很整洁，它的设计是循环的，这是一种无压力的方式来驱动步进电机。它配有一个视频，嵌在下面。

这个时钟由无处不在的 28BYJ-48 步进电机驱动，这种电机只需花几块钱就能在易贝买到。它们没有太大的扭矩，但在这里它们要做的只是转动一个纸板圆盘。真是绝配。

不过，这些马达有一个警告:它们每转没有整数步数。如果你有“1:64”齿轮版本，它实际上是齿轮 8910:567424。结果如何？你需要 2037.8864 步，而不是每圈 2048 步。如果做错了，12 小时的轮子每天会浪费 14 分钟。

因此，在驱动电机、低扭矩和非整体传动装置之间，需要学习的东西比你想象的要多。如果你想要精确，你可以增加一个实时时钟电路。有了这些可以扩展的空间，你只需要花几块钱就可以在一个周末建成并运行它。这使它成为完美的“你好世界”。

 [https://www.youtube.com/embed/Qys5OIncymw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Qys5OIncymw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 步进电机？编码器？都是！

> 原文：<https://hackaday.com/2018/07/15/stepper-motor-encoder-its-both/>

我们总是觉得有趣的是，一台普通的 DC 发动机和一台发电机差不多是一回事。当然，每一个都是为其目的而优化的，但是除了低效率，你可以用电来旋转轴或者用旋转轴来发电。[Andriyf1]有一个稍微不同的窍门。他展示了如何使用步进电机作为编码器。你可以在下面看到设置的视频。

有道理。如果步进器中的线圈可以移动轴，那么移动轴应该会在线圈中感应出电流。然而，他确实注意到，在低速时，你可能会错过脉冲。同样，该设备并没有真正优化这种类型的操作。

该电路使用基于运算放大器的差分放大器从线圈读取脉冲。两个线圈上的两个运算放大器产生一个正交信号，就像普通编码器一样。当轴朝一个方向转动时，一个脉冲将领先于另一个脉冲。在另一个方向上，超前脉冲将反向。

有代码让 Arduino 读取脉冲。这里有很多代码可以在 Arduino 或其他处理器上读取正交信号。顺便说一下，我们已经看到类似的黑客用[硬盘电机](https://hackaday.com/2018/01/07/scrap-a-hard-drive-build-a-rotary-encoder/)做的，它们非常相似。

 [https://www.youtube.com/embed/fQ19661UGx8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fQ19661UGx8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


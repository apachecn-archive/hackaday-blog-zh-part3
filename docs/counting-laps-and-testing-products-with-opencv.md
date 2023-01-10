# 用 OpenCV 计算圈数和测试产品

> 原文：<https://hackaday.com/2016/12/30/counting-laps-and-testing-products-with-opencv/>

自从 Batteroo(正式名称为 Batteriser)被宣布为众筹项目以来，已经过去了大约一年半的时间。前提是围绕 AA 和 AAA 电池的一个小套筒，提高电压以提取更多的寿命。EEVblog 的[达夫·琼斯]是许多质疑产品的人之一，该产品声称可以将电池寿命提高 800%。

Batteroo 确实设法做了许多众筹项目做不到的事情:交付产品。现在这些袖子已经送到支持者手中，人们开始在野外测试它们。事实上，EEVblog 上有一个完整的[测试线程](http://www.eevblog.com/forum/projects/batteroo-testing/)。

正在进行的一项测试是一辆电池供电的火车，沿着轨道行驶，直到电池完全耗尽。[弗兰克·巴斯]想要进行这项测试，但不想手动计算火车跑了多少圈。他用 Python 和 OpenCV 编写了一个脚本来自动计数。

脚本通过在赛道上设置两个区域来测量圈数。当列车进入第一个区域时，计数器启动。当它通过第二个区域时，该圈被记录下来。每一圈的时间都被记录下来，以确保将电池与普通电池进行比较时获得良好的数据。

这个脚本为想玩计算机视觉的人提供了一个很好的例子。Github 上的[提供了源代码。至于电池，我们将等待进一步的测试结果，然后做出判断，但我们不会屏息以待。毕竟，火车用电池跑了一半的时间。](https://github.com/batterootesting/OpenCV-tests/blob/master/lapcounter.py)
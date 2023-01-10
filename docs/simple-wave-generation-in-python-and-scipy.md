# Python(和 SciPy)中的简单波形生成

> 原文：<https://hackaday.com/2017/06/26/simple-wave-generation-in-python-and-scipy/>

[153Armstrong]发表了一篇关于使用 Python 生成波形有多简单的短文。我们同意这很简单，但实际上，并不是 Python *本身*，而是一些非常酷的库( [SciPy](https://docs.scipy.org/doc/scipy/reference/) )做了所有的艰苦工作。这可能是吹毛求疵，但不值得一提的是，SciPy(发音为“叹息派”)也有其他方便的技巧，如傅立叶变换。你可以在下面看到他的结果的视频。

代码很简单，其中一位评论者指出了一种更有效的方法来将数据写入 WAV 文件。基本思想是使用 SciPy 的 NumPy 组件的一些特性在缓冲区中创建一个样本数组。

使用算法很容易创建大多数规则波形。例如，正弦波一般可以描述为:`y=amplitude * sine(radian_frequency*t+phase_shift)`

其中`y`是波在时间`t`的值。幅度是峰值(所以 5 会给你+/-5 V)，弧度频率是π值的两倍乘以频率(单位为赫兹)。[153Armstrong]使用 SciPy 包提供的生成器显示了正弦波、对称和非对称方波以及锯齿波的简单公式。代码在 [GitHub](https://github.com/makermovement/3.5-Sensor2Phone/blob/master/generate_any_audio.py) 上，他还链接到[SciPy](https://docs.scipy.org/doc/scipy-0.14.0/reference/signal.html#waveforms)中可用的发电机。

我们以前在一些黑客大赛参赛作品中见过 SciPy。你可以把它想象成 Python 的 [Matlab。请记住，它不是 Python 的固有部分。如果您使用另一种语言，您可以使用类似的库来获得相同的效果。如果你用硬件来做这件事，你可能会想使用](https://hackaday.com/2012/08/27/measuring-the-speed-of-sound-with-science-and-statistics/)[查找表](https://hackaday.com/2014/11/24/direct-digital-synthesis-dds-explained-by-bil-herd/)，让事情变得快速简单。

 [https://www.youtube.com/embed/lRQsnn-YFiU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lRQsnn-YFiU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 没有频谱分析仪？没问题！

> 原文：<https://hackaday.com/2015/12/20/no-spectrum-analyser-no-problem/>

在过去糟糕的日子里，频谱分析仪是一台昂贵的大机器，放在你的工作台上示波器旁边。虽然好的示波器仍然要花很多钱，但[rheslip]向你展示了如何把你的 VISA 兼容示波器变成一个不错的频谱分析仪,而且价格非常低。请观看休息时间下方的视频。

如果你的范围相对较新，比如 90 年代末，它可能支持国家仪器的签证:虚拟仪器软件架构。[rheslip]的 Rigol scope 可以，他使用[py VISA，NI-VISA 库的 Python 包装器](https://pyvisa.readthedocs.org/en/stable/)从 scope 下载原始样本，然后在他的笔记本电脑上处理 FFT。

这种方法肯定有缺点。示波器的采样深度是八位，限制了他的最大信噪比，而且数字运算和数据传输比较慢，导致刷新率为 2 Hz。但是一旦数据传到他的笔记本电脑上，[rheslip]就可以以他想要的任何样本长度运行 FFT，从而获得非常高的频率分辨率。

事实上，我们认为可以通过对示波器数据的原始访问进行各种定制过滤和分析。为什么我们一直没有这样做？你们当中有谁有很酷的签证技巧可以分享吗？

 [https://www.youtube.com/embed/twRke3suKpE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/twRke3suKpE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



你可能也会对这个视频感兴趣，他画出了 0-200MHz 的频谱图，这样他就可以更好地隔离当地的调频广播电台。对于一个插在廉价示波器上的天线和一些软件来说，还不算太寒酸。

感谢[冰箱之火]的提示！
# GPS 训练振荡器

> 原文：<https://hackaday.com/2018/06/04/gps-disciplined-oscillators/>

[马丁·洛顿]得到了一个 GPS 控制的振荡器。他不太确定该怎么做，所以他做了一些研究和实验。如果你有大约两个小时的空闲时间，你可以观看他的[视频，在那里他分享了他的结果](https://www.youtube.com/watch?v=JrCmpjZe6bI)(见下文)。

他主要看的是一台 Symmetricom TrueTime XL-DC，即使在易贝也要 500 多美元。然而，[Martin]也在考虑一种更实惠的小户型。

你用这样的东西做什么？这个想法很简单。高质量的晶体(或铷)振荡器被训练成与来自 GPS 或另一种类型的导航卫星的定时信号一致。由于导航卫星保持非常精确，晶体振荡器可以精确到纳秒级。

在军事和商业领域，来自这种振荡器的定时可以同步多个接收机，这对于无源雷达等应用是必要的。GPS 计时本身具有出色的长期稳定性，但由于计时单位是每秒一个脉冲，再加上多路径和其他传播效应等因素，短期稳定性并不总是很好。然而，晶体振荡器具有很好的短期稳定性。它们倾向于随温度漂移(通过烘箱减轻)以及晶体和其它成分的简单老化。将两者结合起来，你可以获得出色的短期表现，这种表现也可以持续很长时间。

取决于它是如何设置的，这样的振荡器在开启后很快就可以精确到万亿分之几的范围内。即使是低端设备也能在十亿分之几的范围内运行。当然，你也需要一个能看到天空的天线。

我们之前报道过从手机网站上黑掉这些东西。如果你感兴趣的话，我们还看到了 [GPS 同步电脑时钟](https://hackaday.com/2017/04/13/apparently-time-is-money/)。

 [https://www.youtube.com/embed/6qm5mv6itZQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6qm5mv6itZQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/JrCmpjZe6bI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JrCmpjZe6bI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


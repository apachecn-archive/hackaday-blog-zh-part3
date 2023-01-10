# 光电二极管放大器电路窥探你的手机

> 原文：<https://hackaday.com/2016/08/06/photodiode-amplifier-circuit-spies-on-your-phone/>

为了帮助他的朋友准备本周末在 DEFCON 上的演讲，[克雷格]建造了一个[红外光电二极管放大器电路](http://www.analogzoo.com/2016/08/photodiode-amplifier-design/)。该电路将黑客的探测范围从几英寸扩大到几英尺。我们喜欢一些设计良好的模拟电路，如果你也是，一定要看看下面的视频。

这个话题是关于通过手机的接近传感器发射的红外线来识别手机。举例来说，这些传感器可以告诉手机手机是否靠近你的耳朵。当然，如果接近传感器中的红外发射器一直在运行，这将是一个电池消耗，所以制造商只是间歇性地打开它们。如果不同的制造商使用不同的模式，你可以对手机进行指纹识别——如果你能从足够远的距离探测到有用的红外线。

这就引出了红外光电探测器放大器。该电路“几乎”是一个简单的运算放大器电流电压(跨阻)放大器。但是有并发症。为了获得非常高的增益，由于光电二极管的固有电容，电路容易振荡，因此反馈环路中有一个阻尼电容。为了避免轨到轨的冲击，[Craig]偏置正输入，并在反馈环路中增加一些二极管，以缩小输出范围。由于输出将进入微控制器，它将通过一个比较器，使其更好地数字化。最后，[克雷格]使用了一个很好的大光电二极管，具有良好的灵敏度。

我们想知道为什么[Craig]花费如此大的精力来保持第一级运算放大器不饱和，而他却用一个比较器来跟随它。有人吗？

无论如何，能够从远处探测红外脉冲是很酷的。你知道你可以用光电二极管来检测(β和γ)辐射吗？关于振荡和信号调理的警告同样适用！

 [https://www.youtube.com/embed/FtdJ4e973bk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FtdJ4e973bk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


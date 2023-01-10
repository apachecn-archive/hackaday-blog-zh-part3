# 过度思考螺线管控制

> 原文：<https://hackaday.com/2016/05/11/overthinking-solenoid-control/>

没有一个电路是如此的微不足道，以至于不值得去认真思考。[查尔斯·威尔金森]想要[驱动一个电磁空气阀](https://charleswilkinson.co.uk/2016/04/27/simple-solenoid-driver/)，它将长时间保持打开。这意味着降低保持电流以防止浪费如此多的功率。他偶然发现了这篇文章，这篇文章说[以荒谬的深度涵盖了一种方法](http://m.electronicdesign.com/analog/what-s-all-solenoid-driver-stuff-anyhow)。

[查尔斯]做了两个关于它的视频，一个是他调试电路并在摄像机前现场学习的视频，另一个是他总结的视频。我们将带你走完这个漫长的过程，但你可以随意跳过。

螺线管最初比保持打开更难打开。所以[查尔斯]把他的螺线管接到可变电源上，测试激活和释放电压——因为没有什么能打败经验数据。他缓慢提升电压(大约 6-7 分钟)，电压在 3.5 V 时跳闸。测试螺线管再次闭合时，他将可变电源降至 1.25 V。总之，你明白了:更高的开启电压，更低的保持电压。

这就是链接文章中鲍勃·皮斯电路的观点。电容器最初通过电流，但随后随着时间的推移充电，使得螺线管上的电压下降较少，从而降低了保持电压。诀窍是选择电阻和电容来匹配你的螺线管的特性。

在视频中，大约 30 分钟后，[Charles]建立了电路，并发现它不起作用。他没有剪辑，而是现场解决问题。(勇敢！)他失败了，下线了。最终的问题？他正在用 USB 给电路断电，同时给他的手机充电。他的电源没有足够的能量。然后，在十多分钟的间歇调试后，他在电源轨上加了一个缓冲电容，问题就消失了。

从这一切中有两点可以吸取。第一种是简单而优雅的电路，可以用来驱动螺线管或继电器或任何具有强大初始电流需求的器件。第二是稳定动力和缓冲的重要性。

 [https://www.youtube.com/embed/mlffhp6CDhg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mlffhp6CDhg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


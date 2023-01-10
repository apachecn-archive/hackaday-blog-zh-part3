# 在你的电视上玩绝地心理战

> 原文：<https://hackaday.com/2018/05/03/playing-jedi-mind-tricks-on-your-tv/>

手势控制意味着你可以实现运用原力的幻想。然而，这确实需要一点黑客技术来实现。直接来自[circuito.io]团队的一款[手势控制器](https://www.circuito.io/blog/gesture-remote-control/)可以让你用绝地思维操控你的设备！

这里展示的明星是 APDS-9960 RGB 和手势传感器，Arduino Pro Mini 328 进行思考，红外发射器 LED 很好地利用了这一点。Arduino 草图是 IR LEDs 和手势传感器的两个代码示例的嵌合体——分别由始终可信赖的 [Ken Shirriff](https://hackaday.com/2018/03/29/eavesdropping-on-a-vga-monitors-conversations/) 和 SparkFun 提供。

当然，您可以让输出触发不同的设备，但由于这种特殊的构建是为了控制电视，团队必须使用单独的 Arduino 和 IR 接收器来发现他们想要使用的命令的代码。一旦它们被添加到草图中，在 X、Y 或 Z 轴上移动你的手到传感器上执行命令。瞧啊。—绝地的力量。

 [https://www.youtube.com/embed/O5AHlrsBKPU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O5AHlrsBKPU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



电源问题意味着该团队需要实现一种“深度睡眠”模式，在检测到手势之前，Arduino 会一直给药，以保持 3.7V LiPo 1000mAh 的电池寿命。他们还推出了一个很酷的可选附件，即倾斜开关，当盒子处于除了向上以外的任何方向时，它也可以将 Arduino 置于睡眠模式！

你多久能黑进一次自己的方式来拥有科幻能力？比你想象的更频繁。
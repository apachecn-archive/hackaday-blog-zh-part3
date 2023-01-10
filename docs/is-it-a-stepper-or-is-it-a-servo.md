# 是踏步机吗？还是伺服？

> 原文：<https://hackaday.com/2016/04/30/is-it-a-stepper-or-is-it-a-servo/>

几乎每个参与 3D 打印的人都会在某个时候想，“这一切都可以用闭环系统和 DC 汽车来完成”。或者至少是我们认识的所有人。甚至有一种商业打印机使用伺服控制，但正因为如此，它与(步进电机驱动的)DIY 生态系统的其余部分不兼容。

[LoboCNC]想要改变这一点，他处于一个独特的位置来做到这一点，之前他已经建立了一个销售基于 PIC 的伺服控制器的业务。他的“ [servololu](http://forums.reprap.org/read.php?1,654278) ”本质上是一个微控制器和 DC 电机驱动器，带有用于反馈的正交编码器的输入。该微处理器采用标准的步进/方向输入，就像你用来驱动步进电机一样，然后将连接的 DC 电机伺服到正确的位置。它甚至会在出错时发出信号。


[LoboCNC]过去工作的不幸副作用意味着他不能发布运行他的演示的代码，但他说他正在开发一个开源的固件版本。请看一个演示视频(下图),这是一台由标准步进电机控制器驱动的改进型伺服打印机。这当然是准确的！

如果你想快速了解步进电机和伺服电机，这个由[Homofaciens]提供的视频教程非常值得你去学习。事实上，它实现了[LoboCNC]的一个(非 PID、原始)版本。这并没有脱离[LoboCNC]的想法:将伺服控制硬塞进现有的步进电机驱动器是一个很好的想法，因为它允许快速试验一种新的电机驱动模式。我们等不及要看这个软件了。

还有谁在他们的 3D 打印机上采取了类似的闭环控制方法？我们几年前就放弃了，认为步进器与完全重新设计的麻烦相比“足够好”，所以如果“servololu”证明我们错了，我们会很高兴。

谢谢[马特]的提示！

 [https://www.youtube.com/embed/8RaU6VGdGVk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8RaU6VGdGVk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 一个真正控制问题的电池极耳焊机

> 原文：<https://hackaday.com/2017/09/16/a-battery-tab-welder-with-real-control-issues/>

点焊应该比看起来容易。毕竟只是短时间内通过一个小空间的大量电流而已。但正是这种控制决定了持续高质量焊接和低性能焊接之间的差异，甚至可能导致火灾。

控制是【WeAreTheWatt】的[下一级电池极耳点焊机](https://www.youtube.com/watch?v=Ceos88VO6p4)发光的地方。事实上，没有一个微波炉变压器是一个好处，任何人对我们通常看到的普通电源供电的点焊机感到害羞，即使是那些设计时考虑到安全的。[WeAreTheWatt]选择用大容量 RC 电池组为他的点焊机供电，但我们打赌任何大电流电源都可以。控制器本身是一个看起来非常坚固的 PCB，具有宽走线和精心加工的黄铜汇流条，支持一系列 MOSFETs。微控制器执行相当多的功能；除了定时脉冲之外，它还可以控制传输的能量，读取 8AWG 导线的电阻以进行校准，甚至检测不良焊接。焊接机通常使用脚踏开关，但它也可以检测引线何时短路，并自动施加脉冲——非常适合大批量生产。请看下面的实际操作。

可能会有更大的焊工(T1)和更适合 T2 的焊工(T3)和完成 T5 的焊工(T4)，但这看起来是一个精心设计的解决方案。

 [https://www.youtube.com/embed/Ceos88VO6p4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ceos88VO6p4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[米克·汉克斯]的提示。
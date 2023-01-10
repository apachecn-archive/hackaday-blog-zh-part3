# 555 种控制 DC 电机速度的方法

> 原文：<https://hackaday.com/2018/06/12/555-ways-to-speed-control-a-dc-motor/>

555 定时器集成电路是一个非常有用的 8 针封装的有源元件。最初是为了计时的目的而设计的，它们变成了无处不在的部件，可以实现几乎任何事情。在这种情况下，它们被用来创建一个基本的 PWM 电机控制器。

诀窍是将 555 设置为不稳定模式，并在充电/放电回路中使用二极管和电位计。通过将二极管挂在电位计的两侧，连接到充电和放电引脚，并将中间接线片连接到主电容，可以改变电容在充电和放电期间的电阻。充电时间越长，脉冲宽度越大，放电时间越长，脉冲宽度越小。实际频率本身很大程度上取决于电容和电位计本身的总电阻。

这是一种非常老式的产生 PWM 信号的方法，可以用来改变光的强度或在蜂鸣器上制造噪音。然而，在这种情况下，555 的输出连接到一个 MOSFET，用于改变计算机风扇电机的速度。

这是一个学习 PWM 电机控制和 555 定时器使用的好方法，所有这些都需要很低的零件成本和现成的元件。我们以前见过这样的设置，也用作易于制造的调光开关。
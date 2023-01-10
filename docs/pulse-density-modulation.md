# 脉冲密度调制

> 原文：<https://hackaday.com/2015/09/08/pulse-density-modulation/>

[sot . Eric]在尝试驱动电机时，很自然地想到了使用脉宽调制(PWM)来控制电机速度。然而，他发现即使有一个大电容，他的供电不足的电源也会在 PWM 周期完成之前下降。所以他决定用脉冲密度调制来代替 PWM。

这个想法是在更长的时间内使用更小的脉冲，并使平均功率等于所需的百分比电机速度。例如，对于 PWM 系统，如果时间周期为 T，则 50% PWM 驱动将使驱动在 T/2 为高电平，在另一半周期为低电平。对于脉冲密度，每个脉冲可能是 T/10(举例来说)，然后输出将为 1/10 开，1/10 关，1/10 开，以此类推，直到时间 T，您仍然可以达到 50%。优点是输出电容更容易受到冲击，下降的机会更少。

你可能需要一个示波器来测量 PWM 或脉冲密度，但我们已经在之前讨论过[如何实现无示波器测量。如果你想去守旧派，想想怎么用 555 芯片](http://hackaday.com/2014/11/26/easy-and-effective-way-to-measure-pwm-without-a-scope/)做脉冲密度[，贴在 Hackaday.io 上](http://hackaday.com/2013/09/15/the-easy-or-hard-way-to-build-a-pwm-dimmer/)

 [https://www.youtube.com/embed/UFT8ZYlntb4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UFT8ZYlntb4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


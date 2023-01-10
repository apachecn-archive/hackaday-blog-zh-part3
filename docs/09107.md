# Arduino 控制

> 原文：<https://hackaday.com/2018/04/14/pid-control-with-arduino/>

经验——或者至少是教育——通常对一个成功的项目有很大的影响。例如，如果你没有想太多，你可能会认为控制正在加热的东西的温度很简单。冷的时候就开暖气，达到合适的温度就关，对吗？这是一种方法，有时被称为 bang-bang，但你会发现这种方法有很多问题。最佳实践是使用 PID 或比例/积分/微分控制。[Electronoob]有一个很好的教程，教你如何用 Arduino 完成这个任务[。你还可以看到一个视频，在下面。](http://electronoobs.com/eng_arduino_tut24.php)

该演示使用 3D 打印机热端、热电偶、读取热电偶的 MAX6675 和 Arduino。还有一个液晶显示器和一个场效应晶体管来控制加热器。

PID 控制器背后的思想是测量当前温度和期望温度之间的差值，即设定值。比例增益告诉你由于这种差异产生了多少输出。因此，如果设定值偏离太远，比例项将向加热器产生大量输出。如果很接近，只会产生一点点输出。这有助于防止温度过高而不得不降下来时的过冲。

根据一段时间内的累积误差，积分项会稍微增加一点输出。导数项对温差的变化起反应。例如，如果外部因素导致温度突然下降，导数项可以增加输出以进行补偿。

然而，关键词是“可以”设置 PID 的一部分是找到每一项的系数，对于某些系统来说，这可能是零甚至是负的(表示相反的效果)。还有许多其他的微妙之处，比如如果输出在很长一段时间内不再影响温度，并且积分量增长到无法控制的数量级，会发生什么。

顺便说一下，我们之前已经为 Arduino 介绍过一个 [PID 库](https://hackaday.com/2011/07/21/demystifying-pid-control-with-a-look-at-the-new-arduino-pid-library/)。虽然这篇文章谈论的是温度，PID 控制被用于从[飞行控制](https://hackaday.com/2014/05/12/a-quadcopter-from-scratch/)到[悬浮](https://hackaday.com/2014/07/02/the-old-ping-pong-ball-levitation-trick/)的一切。

 [https://www.youtube.com/embed/LXhTFBGgskI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LXhTFBGgskI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


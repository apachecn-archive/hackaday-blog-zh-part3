# 无外部模数转换器的视频 FPGA

> 原文：<https://hackaday.com/2015/09/09/video-fpga-with-no-external-ad/>

您有一台带有非标准 RGB 视频输出的旧 PC，您需要将它带到一台现代 PAL 电视机上。这就是[svofski]遇到的问题，所以他决定[使用基于 Altera 的 DE1 板来进行转换](https://github.com/svofski/videoconditioner)。通常情况下，读取 RGB 视频信号需要模数转换器，而 FPGA 通常不具备这种功能。[svofski]没有添加外部设备，而是使用了一个技巧来劫持 FPGA 的 LVDS 接收器，并将它们用作比较器。

该方案确实需要一些分立元件来对输入信号进行电平转换，并提供一个 RC 积分器。积分器用作数模转换器，允许 FPGA 将输入信号与输出电压进行比较。一旦模拟信号被数字化，将其转换成您想要的任何格式都相对简单。回到模拟域就像一个脉冲宽度或[脉冲密度调制](https://hackaday.com/2015/09/08/pulse-density-modulation/)方案和一个 RC 滤波器一样简单(或者你可以使用一个简单的 [R2R DAC](http://hackaday.com/2010/08/17/building-a-discrete-digital-analog-converter/) )。

结果是一个零件数量非常少的项目完成了工作。当然，这是对 FPGA 中 LVDS I/O 的完全破解。如果你想了解更多关于 LVDS 的真实用途，请看下面的视频。

 [https://www.youtube.com/embed/CkpkDSgI3e0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CkpkDSgI3e0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


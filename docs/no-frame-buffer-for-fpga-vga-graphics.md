# FPGA VGA 图形没有帧缓冲

> 原文：<https://hackaday.com/2016/06/16/no-frame-buffer-for-fpga-vga-graphics/>

通常，当你想到用软件或硬件驱动 VGA 时，你会想到使用帧缓冲器。帧缓冲器通常是双端口 RAM。一个硬件或软件进程填充 RAM，另一个进程以正确的速率取出数据，并将其发送到 VGA 显示器(通常通过数模转换器)。

[Connor Archard]和[Noah Levy]想用 DE2-115 FPGA 板做一些音乐处理。为了驱动 VGA 显示器，他们采用了一种新颖的方法。他们使用 FPGA 实时计算每个像素的数据，而不是帧缓冲器。

我们不确定为什么，但这个项目被命名为“俱乐部中的布鲁斯”，尽管我们怀疑它与[布鲁斯之地]有关。它通过编解码器将音频读入 DE2-115，经过过滤后提供给图形引擎。屏幕上有四个随着音乐起舞的舞者。检测到的最低频率代表允许舞蹈与音乐同步的歌曲节拍。FPGA 一次可以在屏幕上跟踪多达 64 个对象，包括深度。

[Conner]和[Noah]详细描述了该系统，您还可以在下面看到视频演示。[Bruce]在康奈尔大学的 FPGA 课程中有很多好东西，包括这个[超快速 FPGA 音频可视化](http://hackaday.com/2016/06/13/fpga-powers-blazingly-fast-led-matrix-audio-visualizer/)和这个[全 FPGA VGA 手指跟踪游戏](https://hackaday.com/2016/06/04/real-time-fpga-finger-detection/)。

 [https://www.youtube.com/embed/RYJPcRr-yeI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLzdPghmYexriGUsJQ83yOziJBiYHRooXf](https://www.youtube.com/embed/RYJPcRr-yeI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLzdPghmYexriGUsJQ83yOziJBiYHRooXf)


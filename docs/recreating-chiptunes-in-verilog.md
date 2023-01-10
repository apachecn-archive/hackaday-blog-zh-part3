# 在 Verilog 中重建 Chiptunes

> 原文：<https://hackaday.com/2016/06/19/recreating-chiptunes-in-verilog/>

康奈尔大学的学期即将结束，这意味着是时候进行[布鲁斯·兰德]实验室的期末项目了。每年我们都会看到一些非常酷的项目，今年也不例外。在他们的项目中，[Andre]和[Scott] [实现了任天堂娱乐系统(NES)](https://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2016/avh34_sz296/ece5760_Final_Project_avh34_sz296/ece5760_Final_Project_avh34_sz296/ece5760.Final.Project.Report/ece5760.Final.Project.Report.html) 的音频处理单元(APU)。这是经典的 chiptune 声音，在并非真正 6502 CPU 的 6502 CPU 的帮助下，用并非真正 8 位的 8 位声音取悦了一代人。

与同时代的 MOS 6581 SID 不同，它基本上是一个芯片上的模拟合成器，NES 中的 APU 非常简单。有两个脉冲波通道、一个三角波通道、一个随机噪声通道和一个很少使用的用于播放极低质量音频样本的增量调制通道(DMC)。这是一个大学实验室的 NES APU 的重新实现；很容易理解[Andre]和[Scott]没有实现很少使用的 DMC。

关于 NES 电路的一切都被很好地记录了下来，所以[Andre]和[Scott]有一个很棒的 wiki 来进行他们的研究。在最高级别，APU 运行在 894kHz 时钟上，并通过专用寄存器控制三个通道。这些输出通过混音器输入，这些人将它们缩放并组合成 16 位输出，通过 Wolfson WM8731 音频编解码器播放。

在实现了 NES APU 之后，[Andre]和[Scott]添加了一个可以读取任天堂声音格式(NES chiptunes 的标准发行格式)的 SD 读卡器，并模拟了一个 6502 来控制寄存器。结果是一个相对简单的设备，以惊人的准确性播放 NES 芯片曲调。项目报告上的声音文件听起来像真实的东西，但这完全是在现代硬件上模拟的。
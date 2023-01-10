# Apple II FPGA

> 原文：<https://hackaday.com/2017/10/10/apple-ii-fpga/>

有一年圣诞节，我有时间。所以他拿了一块 DE2 FPGA 板，用 VHDL 建立了一个苹果 II+电脑的忠实复制品。他将 VHDL 模块用于 6502 CPU 和 PS/2 键盘，并更专注于视频硬件和磁盘仿真。

根据[斯蒂芬]的说法，你可以把 Apple II 想象成一个视频显示器，恰好里面有一台电脑。主时钟是色同步频率的倍数，时序完全围绕视频生成。[Stephen 的]实现模仿了时序，尽管使用了更现代的 FPGA 适当的方法。

FPGA 还有一个只读磁盘仿真器。图像驻留在 SD 卡上，SPI 接口根据需要将其载入存储器。

DE2 主板并不是最便宜的，尽管如果你是学生，你可以得到优惠(大约 200 美元而不是 400 美元)。不过，它们在学校里经常被使用，以至于你经常可以在二手市场上以很低的价格买到它们。此外，有很多价格更低的板采用相同的 Altera FPGA，使用起来应该相当简单。

[Stephen]指出，FPGA 版本比真正的 Apple II+耗电更少，也比模拟 Apple II+的 PC 耗电更少，尽管——正如他指出的那样——这很不公平，因为 PC 有很多与模拟无关的开销。

当然，你可以在[更小的硬件](https://hackaday.com/2017/06/13/the-mini-apple-iie-that-runs-on-c-h-i-p/)上模拟同类型的机器。我们甚至看到了一个基于 [AVR 处理器](https://hackaday.com/2016/12/19/portable-apple-ii-on-an-avr/)的。
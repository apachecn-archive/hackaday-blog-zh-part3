# 第四代片上系统将我们带回到 80 年代

> 原文：<https://hackaday.com/2018/02/22/forth-system-on-chip-takes-us-back-to-the-80s/>

对于任何曾经接触过编程语言的人来说，你很可能是在 80 年代接触到这种语言的。但是，由于这种语言仍然在许多应用程序中使用，您可能不会像有些人那样对这种语言有这种怀旧的感觉。尽管如此，你可能想试试[Richard]的实现，它使用这种独特的语言模拟了 80 年代的微型计算机。

该系统具有用 Verilog 编写的基于 FPGA 的 CPU。它运行在 Nexys-3 板上，具有 PS/2 键盘输入、带 VHDL VT100 终端仿真模块的 VGA 输出、对 Flash 和板载 SRAM 的访问以及 UART。把所有这些放在一起，它实际上是一个基于 Forth 的时间机器。即使您只是好奇它是如何工作的，并且不打算自己构建，它也有非常好的文档记录。

该项目还包括一个用 C 语言编写的 CPU 模拟器，如果你没有构建实际计算机的硬件，它可以模拟整个计算机。[Richard]还在 GitHub 页面上发布了推出自己的第四台电脑所需的一切。不过，还有其他方法可以追溯到 20 世纪 80 年代，比如[使用古怪的 Parralax 推进器](https://hackaday.com/2012/06/08/building-a-1980s-microcomputer-with-a-parallax-propeller/)。
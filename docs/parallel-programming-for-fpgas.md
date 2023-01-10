# FPGAs 并行编程

> 原文：<https://hackaday.com/2018/05/19/parallel-programming-for-fpgas/>

使用 FPGAs 进行设计的最佳特性之一是固有的并行性。当然，您可以编写软件来利用多个 CPU。但是有了 FPGA，你可以享受大规模的并行处理，因为所有的部分都是硬件。你房子里的每一个电灯开关都是和其他的平行运作的。有一本书的新版本，名为[*FPGA*](https://arxiv.org/abs/1805.03648)并行编程，深入探讨了这个主题，它是在知识共享许可下。特别是，这本书侧重于使用 Vivado HLS，而不是更传统的 Verilog 或 VHDL。

HLS 允许设计人员用 C、C++或 SystemC 来表达高级算法。给定更多的信息，HLS 会将其转换成 FPGA 配置。然而，这并不意味着你可以剪切和粘贴普通的 C 代码。HLS 有几个限制，因为它编译的是逻辑门，而不是代码行。实际上，它也生成 Verilog 或 VHDL，但是如果你做得对，那对你应该是透明的。

在介绍之后，这本书更像是一系列关于非常具体的主题的专著，但每一部的深度都令人印象深刻。当然，DSP 的例子很多。还有普通数学，所以如果你想知道如何在 FPGA 中计算正弦或余弦，请阅读第 3 章。

第 9 章对视频处理的讨论将会很有趣，其中也讨论了排序算法和霍夫曼编码。

HLS 是一个很好的工具，但是我们担心它会让人们更加困惑。FPGAs 不运行软件(除非你在上面构建了一个 CPU)，但是很多人把 HDL 描述误认为是软件，因为它们表面上看起来很相似。HLS 使它变得更糟，因为它实际上是 C 或 C++代码。但是它不像普通程序那样编译成目标代码。当然，只有当你必须说服客户或经理你不能将某些软件方法应用于 FPGA 开发时，这才是一个问题。对于实际使用来说，HLS 很棒，可以大大简化开发。

作为 HLS 的一个例子，这里有一个 FFT，不可否认，它使用了一些其他的 C 函数。但是它比用 VHDL 或 Verilog 编写的类似代码更直观——尤其是如果你是程序员的话。

```
void fft(DTYPE X R[SIZE], DTYPE X I[SIZE], DTYPE OUT R[SIZE], DTYPE OUT I[SIZE])
{
#pragma HLS dataflow
DTYPE Stage1 R[SIZE], Stage1 I[SIZE];
DTYPE Stage2 R[SIZE], Stage2 I[SIZE];
DTYPE Stage3 R[SIZE], Stage3 I[SIZE];
bit reverse(X R, X I, Stage1 R, Stage1 I);
fft stage one(Stage1 R, Stage1 I, Stage2 R, Stage2 I);
fft stages two(Stage2 R, Stage2 I, Stage3 R, Stage3 R);
fft stage three(Stage3 R, Stage3 I, OUT R, OUT I);
}
```

这本书是大学课本，所以不是轻松读物。尽管如此，这是一个很好的话题，价格是正确的。

如果你想要更温和的介绍经典 FPGA 开发，我们有。还有其他方法可以将 T2 C 转换成 FPGA T3。
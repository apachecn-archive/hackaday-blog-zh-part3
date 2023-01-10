# 带 Cynth 的 C 语言 FPGAs

> 原文：<https://hackaday.com/2017/04/26/fpgas-in-c-with-cynth/>

用 Verilog 编程 FPGA 看起来很像编程。但事实并非如此，至少不是传统意义上的。已经有几个系统致力于将 C 代码转换成硬件描述语言。其中一个叫 [cynth](https://github.com/cseed/cynth) ，使用简单，可以在 GitHub 上获得。如果你想尝试的话，你需要安装 scala 和一个名为 [sbt](http://www.scala-sbt.org/) 的构建系统。

当然，这也有局限性。如果你想要一个预处理器，你必须单独运行它。你不能使用全局变量、乘法、浮点和 C 语言的许多其他部分。编译器为每个 C 函数生成一个 Verilog 文件。

传统的 C 程序一次执行一件事，除非你在多处理器上使用特殊的技术。即使这样，对于您可能控制的 CPU 数量也有一些实际限制。另一方面，FPGA 允许你实现并行发生的事情。例如，考虑以下情况:

```
while (1)
   {
     out1=ctr1++;
     out2=ctr2++;
   }
```

out1 的值会比 out2 的值稍有变化。如果你有一堆这样的东西，比如高达 999，延迟可能会很大。等效的 Verilog 代码可能如下所示:

```
always @(posedge clk)
begin
   out1<=ctr1;
   ctr1<=ctr1+1;
   out2<=ctr2;
   ctr2<=ctr2+1;
end
```

这看起来几乎一样，但无论有多少，输出都会同时改变。更重要的是，其他所有你看不到的事情也会同时发生。就像硬件与门不“扫描”它的输入一样，FPGA 处理它的所有输入并产生输出。

在 cynth 的例子中，每个 C 函数创建一个 Verilog 模块，该模块具有与函数相同的参数，以及另一个参数来代表返回值(如果有的话)。还会有系统时钟、复位信号和三个控制信号的输入。一个是允许处理的输入。有两个输出。一个指示该功能可启用，另一个指示结果可用。

代码提供的示例是一个驱动四个 led 的赛昂眼图。有两个外部函数是用纯 Verilog 创建的。write_leds 功能驱动 led，sleep 功能产生延迟。

C 代码是一个简单的函数，名为 roving:

```
 while (1)
 {
 if (dir && c == 8)
 dir = 0;
 else if (!dir && c == 1)
 dir = 1;

 if (dir)
 c <<= 1;
 else
 c >>= 1;

 write_leds(c);

 sleep(1000); // 1s
 }
```

相应的 Verilog 文件执行相同的功能，您可以使用 Verilog 仿真器进行验证。

如果你想深入挖掘生成的代码，可以通过一些项目了解更多关于 [Verilog 的内容。如果你不喜欢 C，你可以试试](https://hackaday.com/2015/08/19/learning-verilog-on-a-25-fpga-part-i/) [Python](https://hackaday.com/2012/06/11/programming-fpgas-with-python/) 。
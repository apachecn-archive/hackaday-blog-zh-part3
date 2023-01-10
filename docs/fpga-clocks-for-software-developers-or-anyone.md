# 面向软件开发人员(或任何人)的 FPGA 时钟

> 原文：<https://hackaday.com/2017/09/21/fpga-clocks-for-software-developers-or-anyone/>

以前是设计硬件需要原理图，设计软件需要代码。当然，很多人可以来回跳，但这显然是一个不同的学科。今天，许多实质性的数字设计都是使用硬件描述语言(HDL)进行的，如 Verilog 或 VHDL。这些看起来像软件，但正如我们多次指出的，它们并不完全相同。[zipcup]有一篇非常清晰的博客文章，解释了[与众不同之处以及为什么](http://zipcpu.com/blog/2017/09/18/clocks-for-sw-engineers.html)。

[zipcup]记录了一些我们在网上经常看到的东西。一些新手将使用 Verilog 或 VHDL 编写顺序代码，就好像它是一种传统的编程语言一样。这样的代码甚至可以模拟。然而，最终的硬件在最好的情况下效率非常低，在最坏的情况下甚至无法工作。

我们不太同意帖子中的一句话:“……没有时钟，任何数字逻辑设计都无法工作。”然而，[zipcup]继续阐述，我们同意这种阐述。然而，需要注意的是，异步和组合逻辑并不使用传统意义上的时钟。组合逻辑——例如，一堆 AND 和 or 门——只能处理简单的任务，而成熟的[异步设计](http://apt.cs.manchester.ac.uk/ftp/pub/apt/www/async/async_desc.html)很难，不太可能是新的 FPGA 开发人员会遇到的事情。

事实是，几乎所有重要的数字设计都使用时钟，因为它使设计易于管理。实质上，时钟告诉电路的所有部分开始处理，并为各种组合部分的完成设定一个期限。如果没有时钟，你将不得不处理这样的问题，例如，在另一级的进位到达之前，加法器给出一个结果来改变这个答案。有了时钟，只要正确的答案在时钟边缘准备好了，你就不用关心到底需要多长时间。

这一点尤其重要，因为 Verilog 和 VHDL 并不像软件开发人员预期的那样逐行执行。相反，HDL 结构变成了电路，所有的电路同时工作。这种并行性可能很难管理，但它使 FPGAs 成为高速计算和快速响应时间的理想选择。

这篇文章中关于在时钟之间放置多少逻辑的部分就是你通常所说的“定时”关于信号从 FPGA 的一个部分传输到另一个部分需要多少时间，FPGA 工具有数量惊人的数据。如果工具检测到两个时钟元件之间的传输时间超过了时钟周期，它会将其标记为错误。您可以提高时钟速度，或者从物理上或逻辑上缩短路径。

总的来说，这是对一个棘手问题的极好介绍，其中有许多现实世界的建议。如果你想阅读我们的观点，我们用便宜的格子冰棍板做了一个多部分的 Verilog 教程。还有一个[的实际例子](https://hackaday.com/2015/12/16/taking-the-pulse-width-modulation-of-an-fpga/)使用了同一块板。该教程甚至有一些视频，第一个出现在下面。

 [https://www.youtube.com/embed/Oq8Z0eK0Fmg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Oq8Z0eK0Fmg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


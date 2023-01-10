# 谷歌表单中的虚拟机

> 原文：<https://hackaday.com/2017/07/05/a-virtual-machine-in-google-sheets/>

在过去的几十年里，我们已经习惯了浏览器接管如此多的桌面功能，而这些功能我们过去依赖于独立的软件。多亏了普通的科技公司，电子邮件客户端、日历、办公套件等等现在都可以在云端找到。

有时，这些基于云的桌面软件替代品可能有点粗糙，但通常它们的功能可能会让你感到惊讶，因为它们逐渐接近它们试图取代的软件包。例如，Google Docs 有一个全功能的内置脚本语言，叫做 Apps Script，它可以让你在一点 Javascript 的帮助下完全控制一个文档或电子表格。当[布莱恩·斯蒂芬斯]看到这个时，激起了他的兴趣，所以当然他不得不用他的话说“用它做些奇怪的事情”。他的努力成果是 [Google Sheets 虚拟机](https://briansteffens.github.io/2017/07/03/google-sheets-virtual-machine.html)，这是一台软件虚拟计算机，使用电子表格单元格作为内存、堆栈和寄存器。

由于只有 100 个单元的内存，并且完全依赖于主机浏览器的处理能力，这台机器不可能引起轰动。他给出了完整的指令集细节，有几个演示程序，一个 Fib ~~r~~ 奥纳契数列生成器和一个阶乘生成器，但它普遍缺乏动力并不是重点。相反，它的价值在于优雅地展示了虚拟计算机可以在最不可能的地方建造，对于那些有兴趣窥视其代码的人来说，这可能是如何实现的。

【via [黑客新闻】](https://news.ycombinator.com/item?id=14701460)
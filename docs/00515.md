# IBM 1401 独特的准二进制算法

> 原文：<https://hackaday.com/2015/11/05/the-ibm-1401s-unique-qui-binary-arithmetic/>

旧的大型计算机很有趣，尤其是对我们这些没有亲眼看到它们运行的人来说。我们和老人们坐在一起，听他们讲述过去美好时光的故事。他们告诉我们如何装载纸带，或者用拨动开关和 LED 输出指示器一次发出一个指令。我们抓住每一个词，因为知道我们如何在技术时间线中走到这一步是很有趣的，我们欣赏在“美好的旧时光”中坚持下去所需要的耐心和疯狂。

[Ken Shirriff]正在通过一系列与他在计算机历史博物馆的硬件工作相关的文章，让那些美好的日子变得生动起来。他的最新文章是[一篇描述 IBM 1401 的快速二进制算法](http://www.righto.com/2015/10/qui-binary-arithmetic-how-1960s-ibm.html)的奇怪实现的文章。完全披露:还没有证实[Ken]是一个“老前辈”,但是他的文章并没有帮助证明他不是。

Ken 详细描述了 IBM 1401——于 1959 年首次推出——如何将十进制数作为输入，并一次处理一个 BCD 数字。在执行指令之前，BCD 数被转换成半二进制。Qui-binary 用 7 位表示， 5 个 Qui 位和 2 个二进制位:0000000。qui 部分表示 BCD 值中包含的最大偶数，如果 BCD 值是奇数，二进制部分表示 1，如果是偶数，则表示 0。例如，如果 BCD 号为 9，则 Q8 位和 B1 位被置位，导致: 10000 10 。

由于只应设置一个 qui 位并且只应设置一个二进制位，所以 qui-二进制表示便于错误检查。[Ken]在他的帖子中继续解释 IBM 1401 中更复杂的算法和电路。

如果你不熟悉[Ken]，我们报道了他对[Sinclair 科学计算器](http://hackaday.com/2013/08/30/ken-shirriff-completely-reverse-engineers-the-1974-sinclair-scientific-calculator/)的逆向工程，他对 TL 431 的[解释，当然还有作为他计算机历史博物馆工作一部分的](http://hackaday.com/2014/05/26/ken-shirriff-explains-the-tl431/)[核心内存修复](https://hackaday.com/2015/10/19/repairing-55000-of-vintage-core-memory/)。

谢谢你的提示。
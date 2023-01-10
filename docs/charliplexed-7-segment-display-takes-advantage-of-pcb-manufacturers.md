# Charliplexed 7 段显示器利用 PCB 制造商的优势

> 原文：<https://hackaday.com/2016/08/23/charliplexed-7-segment-display-takes-advantage-of-pcb-manufacturers/>

切割出精确的形状需要稳定的手、激光切割机或数控铣床，对吗？没有。所有你需要的是 PCB 设计软件和制造设施，将为你做铣削。那是【bobricius】非常讨喜的[七段展示设计](https://hackaday.io/project/10280-4-digit-charlieplexed-segment-display)中的秘制酱料。

除了图片和电路板文件，他的 Hackaday.io 条目没有太多细节，但我们也不确定我们需要那么多。三板堆叠中最下面的板有[个多路复用 led](http://hackaday.com/2013/04/08/another-way-to-look-at-charlieplexing/)分支到六个控制引脚。接下来是定制走线隔离板，即由 PCB 公司定制走线。堆叠中最上面的电路板是另一个 PCB，这一个在光线照射的地方没有铜。

我们想看这东西被点燃！在我们之前，我们已经尝试过使用 PCB 环氧树脂材料作为 LED 扩散器，它看起来真的很棒。间隔物应该有助于使片段内的照明均匀，同时防止它们之间的渗色。下一步？WS2812s 矩阵，带有定制路线的垫片和扩散器。那该多棒啊。
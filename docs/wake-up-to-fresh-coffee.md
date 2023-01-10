# 醒来就能喝到新鲜咖啡！

> 原文：<https://hackaday.com/2017/05/21/wake-up-to-fresh-coffee/>

小心你说的话当你看到一个你认为你可以自己制造的商业产品时，你可能会发现自己不得不兑现你的承诺。

当有人向他展示众筹的闹钟咖啡机时，[杨奇煜-乔托]说“只要给我一台浓缩咖啡机，我也能做同样的事情”。一台 Nespresso 胶囊咖啡机适时出现在他的工作台上，所以是时候兑现承诺了。

Nespresso 机器的操作非常简单，前面有一个大杠杆，可以打开胶囊槽，让用过的胶囊落入漏斗中。放入一个新胶囊，拉下控制杆将其装入机械装置，然后按下其中一个按钮，告诉它自己灌注。一分钟后，你可以按下大杯或小杯的按钮，你的咖啡就会送到。

为了用闹钟自动完成这一点，没有必要操作杠杆，让用户来装载胶囊是安全的。因此，时钟所要做的就是通过操作按钮来触发过程。用万用表在按钮 PCB 上快速调查发现，存在的电压为 15 V，远高于 STM32F469 板为时钟指定的逻辑电平。因此，设计了一个简单的电路，使用 MOSFET 来进行开关。

最后，为 STM32F469 开发了时钟软件。该芯片的 2D 图形加速硬件和开发板的高质量显示器确实造就了一个非常光滑的界面。

你可以在休息时间下方的视频中看到结果时钟。这是一个闹钟咖啡机，我们会很自豪地把它放在我们的床边，但有一个小小的担心。在 Nespresso 等市电供电设备上，低压轨并不总是与市电隔离，不清楚是否如此。为了以防万一，我们可能会集成一个光隔离器。

 [https://www.youtube.com/embed/w7NEzSnPe70?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w7NEzSnPe70?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Nespresso 机器以前在这里出现过几次，从[绕过烦人的安全螺丝](http://hackaday.com/2016/08/28/the-most-traveled-security-screwdriver-a-hackers-tale/)，到识别[你面前有哪些彩色编码但烦人的无标签胶囊的便捷工具](http://hackaday.com/2017/02/19/nespresso-capsule-detector/)。
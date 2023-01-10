# 漂移仪器提供了学习晶体振荡器的机会

> 原文：<https://hackaday.com/2018/06/05/drifting-instrument-presents-opportunity-to-learn-about-crystal-oscillators/>

当然，我们都喜欢修理东西，但在值得修理的东西和从长远来看更便宜的东西之间往往有一条细微的界限。然而，当从修复中可以学到一些东西时，这一界限就变得模糊了。

这个不稳定的温度补偿晶体振荡器是一个很好的例子，它倾向于修复只是为了有机会窥视内部。[Kerry Wong]认为这是可编程频率计数器读数过低背后的问题。TCXO 应该输出一个固定频率的信号，该信号在一定温度范围内保持稳定，方法是使用温度传感器来调整压控振荡器，该振荡器可以校正晶体在变热或变冷时改变频率的自然趋势。但是这个 TCXO 太老了，甚至提供的微调电容器也不足以将它推回到范围内。[Kerry]对这个案例做了一些 Dremel 手术，并得出结论，在晶体的一个引线和地之间添加另一个装饰帽会有所帮助。这给了他更宽的调整范围，让他能够将焦点对准正确的 10 MHz 设置。不过,(墨菲先生)仍然在主持这个节目——在他把 TCXO 和新的修剪器《难以接近》合上之后，他发现频率不太对。但是从 2 kHz 到只有 2 Hz 仍然很不错。

无论是[微波电子的怪异世界](https://hackaday.com/2017/09/11/doppler-module-teardown-reveals-the-weird-world-of-microwave-electronics/)还是[建造一个全屋电池库](https://hackaday.com/2017/09/14/battery-management-module-hacked-for-lithium-iron-battery-bank/)，观看【凯瑞】的视频总是很有趣，我们通常最终会学到一两件事。

 [https://www.youtube.com/embed/9L3w3AFJ1Sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9L3w3AFJ1Sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


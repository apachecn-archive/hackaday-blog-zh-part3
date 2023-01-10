# 世界上最薄的莫尔斯电码触控板

> 原文：<https://hackaday.com/2017/02/18/worlds-thinnest-morse-code-touch-paddle/>

莫尔斯电码爱好者可以对他们的拨片吹毛求疵。毕竟他们是人和机器的接口，有经验的电报员可以通过“手”认出对方。因此，尽管[埃德加]一开始用的是便宜的、咔嗒作响的桨，但不久他就自己做出了更好的桨。在这个过程中，他还制作了我们认为可能是最薄的桨，是一片 FR4 PCB 材料和一个纽扣电池。这将是一个袖珍 QRP(低功率)钻机完美。看看下面的视频。

莫尔斯电码桨没什么了不起的。当然，它可以像两个开关一样简单——一个用于“dit ”,一个用于“dah”。你可以用回形针做一个。[Edgar]的版本用电容感应代替了开关，由 ATtiny4 在船上完成。因为这是 1kB 挑战中的一个参赛项目，他优先考虑代码大小而不是特性，并将其缩减到可笑的 126 字节！即便如此，它也有自动重复等豪华功能。我们必须深入研究代码，看看它是否是[抑扬格](https://en.wikipedia.org/wiki/Telegraph_key#Iambic_.28dual-lever.29_Paddles)。

当然，我们以前见过[电容式触摸传感器拨片](http://hackaday.com/2012/04/21/using-a-touch-sensor-as-a-telegraph-key/)。事实上，[不止一次](http://hackaday.com/2011/12/05/an-iambic-keyer-in-5-minutes/)。但是这一个执行得非常好，是一个漂亮的整体解决方案。

DIY 莫尔斯电码桨是一个非常简单的项目，它是你自己建造的无线电小屋的一部分。基本上固件定义了一切，这意味着你可以定制它来适应你的技能和愿望。

 [https://www.youtube.com/embed/iQECz1z8kvE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iQECz1z8kvE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


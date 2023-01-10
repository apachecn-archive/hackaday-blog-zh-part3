# 从网络到 Arduino 的串行数据

> 原文：<https://hackaday.com/2015/10/10/serial-data-from-the-web-to-an-arduino/>

在过去，一个串行端口通常连接到一个声学耦合器，该耦合器可以抓住电话听筒，并允许以 300 波特或更低的速度远程连接到远处的串行端口(通过另一个电话和声学耦合器)。声音耦合器会将串行数据转换成音频，并在通过电话线传输后重新组合。调制解调器有所进步，但大多已让位于 DSL、电缆、光纤和其他高速网络选项。

在一次明显的复古行动中，[詹姆斯·哈利迪]和[牛肉干]给这个古老的想法注入了现代元素。他们使用 webaudio API 向远程 Arduino 发送串行数据。黑客使用一个场效应晶体管、一个电容和几个电阻。他们没有用音频建立一个真正的调制解调器。相反，他们基本上欺骗音频端口发送串行数据，并用外部电路恢复它。到目前为止，他们还只实现了串行发送(所以 Arduino 接收),尽管他们提到下一步将建立连接的另一端。

他们说数据传输很挑剔，但它很有效(见下面的视频)。我们想象使用适当的调制解调器音调和解码器可能会工作得更好，但会更加努力。我们之前已经介绍过一个 1200 波特的调制解调器。我们也涉及了一些[和它们背后的理论](http://hackaday.com/2013/01/31/how-a-dial-up-modem-handshake-works/)。

 [https://www.youtube.com/embed/a8VLnap86pA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a8VLnap86pA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


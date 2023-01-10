# 触摸板远程 MIDI/模拟控制器摇动

> 原文：<https://hackaday.com/2016/06/25/touchpad-remote-midianalog-controller-rocks/>

[酸波旁]手头有一些很酷的部件，一位音乐家朋友需要一个无线电控制的触摸感应 MIDI(和模拟)控制器。今天是黑客日，你可以猜到接下来发生了什么。

[远程表情控制器](https://acidbourbon.wordpress.com/2016/05/26/touchpad-as-wireless-midi-expression-controller/)是一个可爱的小黑客。它始于从德国一家盈余商店购买的触摸板，以及[酸波旁]在德国最大的嵌入式论坛上找到的[的一些代码。几个很好的自制电路板之后，他开始写代码。](http://www.mikrocontroller.net/topic/147076)

如果你想看的话，可以在他的 GitHub 上找到。传输协议本身很简单。它发送一个两字节的报头来检测消息的开始，然后发送三个字节的数据。接收器将其转换为 MIDI 和控制电压输出。简单又有用。

我们也钦佩使用简单的无线电发射机而不是屈服于和使用 WiFi 的非过度杀伤(以及令人羡慕的电池寿命)。

我们之前报道过 Michael/[acidbourbon]的一些黑客技术，当我们在地下室钻 PCB 的孔时，我们想到最多的是他的[半自动钻床黑客](http://hackaday.com/2015/02/04/semi-auto-pcb-drill-press-makes-drilling-semi-painless/)。继续黑！
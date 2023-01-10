# 三重威胁 RTL-SDR 系统读取集群无线电

> 原文：<https://hackaday.com/2016/03/07/triple-threat-rtl-sdr-system-reads-trunked-radio/>

在过去，如果你想听警察，消防，或其他双向无线电用户，你只需要一个简单的接收器。今天，由于集群无线电系统的采用，你更可能需要一些更有异国情调的东西。要接收控制信道和通话组对话的所有线索，你可能需要一个宽带接收器。

[Luke Berndt]发现他需要 6 MHz 来监听他想要收听的电台。这在专用软件定义无线电(SDR)中很容易实现。然而，[卢克]想使用廉价的 RTL-SDR 和他们的带宽约为 2 兆赫。显而易见的黑客解决方案？[用三个！](http://lukeberndt.com/2016/using-multiple-rtl-sdr-to-capture-a-trunking-system/)

如果你以前没有看过集群系统，它本质上允许大量用户共享相对较少的信道。当有人想通话时，他们会移动到一个未使用的频道进行传输。假设爱丽丝问鲍勃一个问题，而这个问题恰好在 12 频道。鲍勃的回复可能在第 4 频道。爱丽丝的后续报道可能会在第三频道播出。

实际上，这意味着接收信号并不难解码。它很难被发现(并且随着它的跳跃而跟随)。对于多个 SDR 来说，这是一项出色的工作，这种方法甚至减轻了 CPU 的负担，CPU 不必解码对对话不重要的信号。

[Luke]包括[源代码](https://github.com/robotastic/trunk-recorder)，还说明了如何更改加密狗的序列号，因为每个加密狗都必须是唯一的。我们已经看到了太多的[伟大的项目](http://hackaday.com/2015/08/21/decoding-satellite-based-text-messages-with-rtl-sdr-and-hacked-gps/)和 [RTL-SDR](http://hackaday.com/2014/04/17/measuring-frequency-response-with-an-rtl-sdr-dongle-and-a-diode/) ，以至于很难选择我们最喜欢的。尤其令人高兴的是，我们知道加密狗只是用来接收电视的，而且所有这些项目都是黑客。

谢谢你的提示。
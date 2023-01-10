# SDR 嗅探电动门

> 原文：<https://hackaday.com/2017/06/11/sdr-sniffing-electric-gates/>

大多数无线 OEM 硬件传统上使用 433MHz OOK 模块来交换信息。数据流的编码和加密是嵌入式软件设计者的任务。在大多数情况下，系统可能会受到重放攻击，记录并重放 RF 数据包以模拟合法用户。[吉拉德·弗里德]用这种技术黑进了他的停车门，但他决定更进一步，将它连接到互联网上。

他使用 RTL-SDR 加密狗和[jimstudt]的[ook 解码器](https://github.com/jimstudt/ook-decoder)来嗅出星门代码，并使用 Arduino 对该代码进行了测试。最终实施是围绕一个 Onion Omega 完成的，它使用 fast-gpio 二进制直接与 RF 发射器模块通信。互联网连接是使用洋葱云 API 实现的，该 API 用于触发代码的执行，从而发送开门信号。

[Gilad Fride]使用 IFTTT Do 按钮提供 GUI，在下面的视频中，他使用 iPhone 演示了这一操作。该项目可以扩展到通过互联网打开车库门或关闭房间的灯。

如果你想入侵你的家庭安全系统，不要再找了，因为 SDR 在过去已经被用来与无线产品有效地通信。我们希望制造商得到提示，开始使用更好的加密技术。

 [https://www.youtube.com/embed/vpondEu6MWg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vpondEu6MWg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


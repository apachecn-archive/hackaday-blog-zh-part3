# 家酿特别提款权业余无线电在 9 个部分

> 原文：<https://hackaday.com/2018/06/06/homebrew-sdr-ham-radio-in-9-parts/>

它曾经是家酿火腿齿轮意味着简单的东西。几个可以发送连续波的有源设备。也许是带 VFO 的接收器。但是，只有最先进的建设者可以处理大范围的单边带收发器。如今，这一目标仍然不容忽视，但由于专用 IC、高速数字信号处理的便捷性以及软件定义无线电技术的进步，这一目标变得更加容易。[Charlie Morris]决定建造一个包含这些技术的 SSB 钻机，他在一系列九个视频中分享了从设计到操作的整个过程。下面可以看到第一个。

NE612 是流行的 NE602 芯片的后代，它包含一个吉尔伯特单元混频器和一个振荡器，使构建接收机比过去容易得多。这些芯片被设置为直接转换接收器，并馈入 Teensy，后者对恢复的音频进行数字信号处理。

Teensy 的一个优点是它有一个附件音频板，可以轻松地将音频输入和输出连接到设备。DSP 处理接收的音频和发送的音频。还有一些其他库存部件，如 LCD、编码器、扬声器、麦克风等。还有一个数字时钟发生器(Si5351)，但这些都是目前常见的现成东西。

第一个视频有点介绍性，但在第二个视频中，他直接跳到了布线以及所有电路工作的原因。到第三个视频时，接收器实际上正在工作，听起来相当不错。因为接收器需要 I 和 Q 输出，所以实际上有两个 NE612s 以不同相位工作。

 [https://www.youtube.com/embed/J7FEJeCYBpY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/J7FEJeCYBpY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


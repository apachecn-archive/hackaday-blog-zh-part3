# BeagleBone 的 SDR 斗篷

> 原文：<https://hackaday.com/2016/03/23/sdr-cape-for-beaglebone/>

在过去，如果你想听短波，你必须转动一个转盘。后来，你也许可以用键盘输入一个频率。借助现代软件定义无线电(以及合适的硬件)，您可以同时收听整个高频频谱。这是 BeagleBone 的开源子板 [KiwiSDR](http://kiwisdr.com/KiwiSDR/index.html) 背后的想法。

前端频率范围为 10 kHz 至 30 MHz，内置一个工作频率为 65 MHz 的 14 位转换器。板上有一个 Xilinx Artix-7 A35 FPGA 和一个 GPS。这个设计是开源的，在 GitHub 上。

该接口使用 OpenWebRX 项目作为强大的 HTML 5 接口。你可以在下面看到它的操作视频，或者，如果你能得到四个可用插槽中的一个，你可以在线收听。从网络的角度来看，加拿大的演示站对我们来说是最好的。不过也有[纽西兰](http://kiwisdr.com:8073/)和[瑞典](http://kiwisdr.sk3w.se:8073/)的车站。

一次读取一大片频谱是一种不同于我们本月早些时候报道的集群无线电 SDR 的方法。该项目使用多个 SDR 将宽带分成易于处理的部分。你可以用一个 KiwiSDR 来代替一个 [pan adapter](http://hackaday.com/2015/12/19/sdr-pan-adapter/) ，永远不用担心调音的问题。

 [https://www.youtube.com/embed/Jtvti1ElB1Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Jtvti1ElB1Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[迈克]的提示。
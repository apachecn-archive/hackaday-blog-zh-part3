# Bela:实时 BeagleBone 音频/模拟 Cape

> 原文：<https://hackaday.com/2016/04/13/bela-real-time-beaglebone-audioanalog-cape/>

Bela 是 BeagleBone Black 的披肩，面向艺术家和音乐家。实际上，cape 还不到故事的一半——剩下的是一些聪明的软件和实时 Linux 发行版。但是我们太超前了。先说硬件。

首先，cape 有立体声输入和输出以及两个放大扬声器输出。它可以做你所有的音频内容。它还有[两组模拟输入和输出](http://bela.io/audio-vs-analogue.html)，每组能够处理八个信号。在我们看来，这就是贝拉酷的地方。特别是，模拟输出是*而不是* Arduino 风格的“模拟输出”，它实际上是一个数字输出，你可以通过 PWM 来模拟模拟信号。这些是来自 [AD5668 DAC](http://www.analog.com/en/products/digital-to-analog-converters/da-converters/ad5668.html) 的 8 路 16 位输出，这意味着您可以直接使用这些电压，无需滤波。

接下来才是真正的诀窍。所有这些输入和输出外围设备都连接到 [BeagleBone 的可编程实时单元(PRUs)](http://hackaday.com/2014/06/22/an-introduction-to-the-beaglebone-pru/)——一个独立于 CPU 但可以与其一起工作的硬件子系统。PRU 与实时 Linux 内核接口，为您的应用提供亚微秒级响应。这是一件大事，因为许多其他音频处理系统都有几十毫秒甚至更长的延迟，人类开始感觉到轻微的滞后。

这种定制模拟和音频 I/O 的缺点是它还不被内核驱动程序支持，你需要使用他们的“重型音频工具”,将 Pd 程序编译成 C 代码，然后驱动 pru。当然，你也可以自己直接为 PRUs 写。如果你只是想玩 MP3，买一些你有一堆更简单，更好的选择。如果你需要做实时音频安装，Bela 是一个不错的选择。

该项目是开源的，但我们不得不做大量的挖掘工作来找到我们想要的东西。硬件在这里的 zip 文件中，你会在这里找到软件[。](https://code.soundsoftware.ac.uk/projects/beaglert)[演示项目](http://bela.io/made-with-bela/index.html)看起来/听起来很酷，他们的 Kickstarter 长期以来资金过剩，所以我们很有兴趣看看人们用这些做什么。
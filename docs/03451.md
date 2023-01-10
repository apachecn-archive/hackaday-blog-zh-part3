# Hackaday 奖参赛作品:清醒梦研究

> 原文：<https://hackaday.com/2016/09/04/hackaday-prize-entry-lucid-dreaming-research/>

清醒梦是恐怖科幻小说中经常出现的罕见心理现象之一。是的，清醒梦确实存在，将普通梦转变为清醒梦的最好方法之一是专注于特定的物体、声音或气味。[为了他们的 Hackaday 奖参赛作品](https://hackaday.io/project/13285-openld-lucid-dreaming-research-platform)，[Jae]正在建造一个设备，让电子爱好者社区开启清醒梦。这是一个研究平台，允许任何人研究自己的梦想，并进入一个你可以做任何事情的世界。

这个项目的核心是一个 8 通道脑电图，用于测量睡眠期间大脑的电活动。这些 EEG 电极馈入 24 位 ADC，由 ARM Cortex M4F 微控制器每秒采样 250 次。捕捉到的数据被记录或通过蓝牙连接发送到电脑或智能手机，在那里可以播放熟悉的声音(想想《盗梦空间》中的公文包)，或其他一些信号，告诉做梦者他们正在做梦。

我们在过去已经看到了一些类似的构建，最著名的[是一个 NeuroSky MindWave 耳机](http://hackaday.com/2012/12/20/modifying-an-eeg-headset-for-lucid-dreaming/)变成了一个舒适的单通道 EEG 类型的设备。然而，NeuroSky 的硬件是有限的，配备适当的放大器和 ADC 的设置对调试[Jae]两耳之间的耳道空间会有很大帮助。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)
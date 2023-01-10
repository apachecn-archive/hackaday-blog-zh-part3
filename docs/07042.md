# 用 Raspberry Pi 和 RTL-SDR 攻击一些无线设备

> 原文：<https://hackaday.com/2017/09/10/attack-some-wireless-devices-with-a-raspberry-pi-and-an-rtl-sdr/>

如果您拥有一台从 USB 数字电视接收机衍生而来的无处不在的 RTL-SDR 软件定义的无线电接收机，您可能会首先使用它来窥探宽频带，使用大多数 SDR 软件中存在的瀑布视图。由于 RTL 覆盖的 VHF 和 UHF 波段有时有点缺乏信号，所以你有机会找到 ISM 波段之一，因为许多廉价的无线设备都使用它来完成各种日常控制任务。除非你住在荒野深处，否则 ISM 波段嗅探会显示出连续的啁啾声；数字数据的短脉冲串。令人惊讶的是，你不知道的无线电控制设备的数量就在你的周围。

其中一些设备，如汽车安全钥匙，受到滚动加密方案的保护，以阻止潜在的攻击者。但是许多更无害的设备只是在没有最起码的加密的情况下公开发送命令。RTL-SDR.com 的人们张贴了一个指南，在树莓 Pi 上记录这些开放的数据突发，并通过 Pi 本身传输它们来播放它们。

这不是最精细的攻击，因为它所做的只是获取记录的文件，并用[f5eo]RPiTX 软件重新传输它。但他们确实用无线灯泡、门铃、无线继电器和遥控开关插座展示了这一点。由于相关数据以 OOK 或开关键控的形式传输，因此 RPiTX AM 模式代表发射机。

你可以在休息时间下面的视频中看到它的运行。现在，您是否调查过您所在地区的 ISM 波段啁啾声？

 [https://www.youtube.com/embed/ewY-woG1dNw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ewY-woG1dNw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这个[并不是我们带给你的第一个 OOK 数据包克隆项目](https://hackaday.com/2014/08/14/thp-entry-a-433mhz-packet-cloner/)，也许你更愿意去[研究数据包中包含的数据](https://hackaday.com/2015/02/16/using-matlab-and-sdr-to-reverse-engineer-433mhz-messages/)。

谢谢[卡尔]的提示。
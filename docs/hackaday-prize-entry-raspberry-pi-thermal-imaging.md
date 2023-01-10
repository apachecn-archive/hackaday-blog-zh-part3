# Hackaday 奖参赛作品:Raspberry Pi 热成像

> 原文：<https://hackaday.com/2016/09/25/hackaday-prize-entry-raspberry-pi-thermal-imaging/>

热感相机是实验者可以负担得起的理想技术之一。在过去的几年里，我们看到了价格更低廉的相机的出现，以及最近一系列绝对在实验者范围内的热感相机模块的出现。他们可能还没有高分辨率，但他们是一个巨大的进步，而且他们开始出现在像这样的网站上的项目中。

其中一款器件是 Melexis MLX90621，这是一款采用 TO39 can 封装的 16×4 像素热传感器阵列，具有 I2C 接口。这很难是单个数量的冲动购买，也不一定是最便宜的模块，但它的价格足够低，足以让[Alpha Charlie]尝试将其与树莓 Pi 连接，为其可见光相机的照片添加热感相机覆盖。

该模块的连线本身很简单，他已经为它创建了几个软件，可以在他的 GitHub 库上获得。mlxd 是模块的驱动程序守护进程，mixview.py 是 Python 图形叠加脚本，它将热阵列输出置于摄像机输出之上。在休息时间下方的视频中可以看到该设备的运行及其结果。

 [https://www.youtube.com/embed/mnBxZONfxBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mnBxZONfxBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这可能还比不上商业热感相机的结果，但它肯定是一个正在取得进步的领域。因此，期望几年后我们将拥有分辨率高得多的廉价模块并不是不合理的，这个项目应该被视为未来美好事物的标志。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)
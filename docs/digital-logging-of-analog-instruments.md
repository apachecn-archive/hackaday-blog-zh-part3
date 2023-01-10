# 模拟仪器的数字记录

> 原文：<https://hackaday.com/2016/04/16/digital-logging-of-analog-instruments/>

你能找到的唯一有用的数据已经被数字化了，但是数量惊人的计量器和仪表仍然是模拟的。将各种压力计、电表和任何其他模拟仪表数字化的正确解决方案显然是用数字传感器和显示器取代令人讨厌的刻度盘。这并不总是可能的，所以对于[Egar]和[ivodopiviz]的 Hackaday 奖参赛作品，他们想出了一种方法，使用树莓 Pi 和一点计算机视觉将这些旧的模拟仪表转换为数字仪表[。](https://hackaday.io/project/10617-instrument-digitizer-using-computer-vision)

这种仪器数字化仪背后的想法不是取代机械和电子设备，正如我们经常做的那样。相反，这个团队使用 3D 打印支架，将树莓 Pi 和摄像头直接安装在模拟仪表的前面。将这个装置与 OpenCV 结合起来，你就有了一个足够智能的设备，它可以看到表盘上的指针，将其转换成数字，并将其保存到文件中或通过 WiFi 发送出去。

对于[Egar]和[ivodopiviz]承认是相对小众的应用来说，这是一个极其简单的设备。然而，如果你只需要一个月左右的模拟仪表的数字测量，或者你不想弄乱你的蒸汽朋克装饰，这是一个巧妙的构建。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/186c8fd237cf75fd0ea0cc799fcf2eac.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)
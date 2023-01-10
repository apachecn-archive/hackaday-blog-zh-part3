# 肌电图教程让你听你的肌肉

> 原文：<https://hackaday.com/2016/11/20/emg-tutorial-lets-you-listen-to-your-muscles/>

随着可穿戴技术、触觉反馈、可植入设备和假肢的出现，人和机器之间的界限变得越来越难以辨别。如果你打算进入这个领域，你需要了解一点肌电描记术，或者说感知使肌肉燃烧的电信号的技术。这个关于使用 Arduino 捕捉肌电信号的实用教程可能正是你想要的。

在一篇主要作为其他物理治疗师的教程而写的文章中，George Marzloff 博士]涵盖了一些对经验丰富的黑客来说似乎非常基础的内容，但仍然有一些有价值的珍闻。他的教程构建围绕着一个 [MyoWare 肌肉传感器](https://www.adafruit.com/product/2699)和一个 Arduino Uno。该肌肉传感器具有用于心电图类型的三个泡沫电极的卡扣连接器，并输出整流和积分波形，该波形表示传输到肌肉的电信号的包络。Marzloff 博士]的简单草图只是读取传感器的模拟输出，如果它检测到肌肉收缩，就会点亮 LED，但一旦你有了基本的 EMG 接口，天空就是极限。假肢、可穿戴设备、诊断工具、虚拟现实——可能性是无穷无尽的。

我们以前见过一些 EMG 接口，主要是自制类型的，如[这个录音机用于 EMG 测量](https://hackaday.com/2012/06/17/diy-emg-uses-an-audio-recorder/)。并且一定要看看【Bil Herd】的[关于从噪音中挖掘肌电信号的深度讨论](https://hackaday.com/2015/12/29/amplifying-the-bodys-own-electricity/)。
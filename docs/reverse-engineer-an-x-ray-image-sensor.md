# 对 X 射线图像传感器进行逆向工程

> 原文：<https://hackaday.com/2018/03/15/reverse-engineer-an-x-ray-image-sensor/>

如果你想到医用 x 射线，很可能你在想象一个照相底片作为它的成像装置。也许是被你的牙医夹在牙齿上，或者是一张臭名昭著的[托马斯·爱迪生]的助手[克拉伦斯·麦迪逊·戴利]的手的照片。

与摄影的其他部分一样，x 射线成像科学受益于数字技术，现在已经确定的是，你的医院 x 射线很可能被电子成像设备捕获。事实上，这些已经被使用了很长时间，以至于他们的第一代甚至可以被一个实验者以可承受的价格买下，这就是足智多谋的 Lucy Fauth 在 Jana Marie Hemsing 的帮助下所做的事情。他们的奖杯 DigiPan 数字 x 射线图像传感器是他们的，价格约为 100 欧元，尽管它在医学上已经过时，但对 x 射线实验者来说仍有巨大的潜力。

这篇文章是对 x 射线传感器机制的迷人探索，解释了早期设备(如这种设备)实际上是线性 CCD 传感器，它以类似于平板扫描仪中光学传感器的方式跟踪闪烁体层后面的曝光区域。该接口显示为一个 RS422 串行端口，并且发现该设备是一个独立的单元，不需要任何命令来启动扫描。通电后，它会发送一个灰度图像，对非标准串行流进行一点 Sigrok 检查，就可以发现它是直接来自传感器的 12 位数据。从这些开始，他们发展到基于 FPGA 的数据处理器，并以激光切割盒中非常整洁的电源结束了这一切。

人们意识到，x 射线是一种特别危险的实验介质，我们从他们的视频中注意到，他们使用了某种形式的屏蔽。光源是一种在运动医学中使用的手持式荧光镜，可产生窄光束。如果你记得[发现了一个意想不到的游戏机](https://hackaday.com/2017/09/24/game-boy-advance-hiding-in-a-medical-device/)，你会意识到医疗电子似乎是那些地区的一个专业，就像[自动盒子搬运器](https://hackaday.com/2017/12/03/boxes-form-an-orderly-queue-behind-the-armchair/)一样。

 [https://www.youtube.com/embed/FhK-hanAdVs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FhK-hanAdVs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


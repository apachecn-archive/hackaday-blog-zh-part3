# Gameboy 相机成为便携式摄像机

> 原文：<https://hackaday.com/2015/11/03/gameboy-camera-becomes-camcorder/>

[furtek]是一个有奇怪追求的人，主要是让旧技术做奇怪的事情。这让他成为我们的英雄，他的最新项目提升了这种地位:他建造了一个设备，可以将[任天堂 Gameboy 相机盒变成摄像机](http://furrtek.free.fr/?a=gbcc)。他的设备取代了 Gameboy，从相机中捕捉图像，在屏幕上显示并保存到微型 SD 卡中。

在你扔掉手机或 4K 摄像机之前，请记住拍摄的视频是单色的(黑白之间只有 4 级)，分辨率为 128×112 像素，每秒约 14 帧。声音以 8192Hz 捕捉，产生与 Gameboy 闻名的相同的嗡嗡声、颗粒声。虽然不是特别实用，但[furtek]的构建非常令人印象深刻，它是围绕一个[恩智浦 LPC1343 ARM Cortex-M3 MCU](http://www.nxp.com/products/microcontrollers/product_series/lpc1300/) 处理器构建的。该处理器反复从相机请求图像，接收图像，然后将图像和声音收集在一起，形成视频并将其保存到 micro SD 卡中。像往常一样，[furtek]已经向任何想尝试的人提供了[所有的源代码和其他文件。](https://github.com/furrtek/GBCamcorder)

对于那些不熟悉他之前工作的人来说，[furtek]已经做了一些事情，比如让一个[像水手一样说&咒语](http://hackaday.com/2012/12/03/teaching-the-speak-spell-four-and-more-letter-words/)，给一个 Virtualboy 添加一个[VGA](http://hackaday.com/2013/06/17/giving-the-virtualboy-a-vga-out/)，以及黑掉一个[game boy Color 来控制电子货架标签](http://hackaday.com/2014/05/03/game-boy-vs-electronic-shelf-labels/)。

 [https://www.youtube.com/embed/gOtaw834G0g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gOtaw834G0g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


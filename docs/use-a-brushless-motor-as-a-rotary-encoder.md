# 使用无刷电机作为旋转编码器

> 原文：<https://hackaday.com/2017/01/18/use-a-brushless-motor-as-a-rotary-encoder/>

电动机是几乎所有机器人项目的基本组成部分，但如果没有某种形式的反馈，它就缺乏任务所需的精确位置控制。来自建模世界的小型伺服系统通常使用电位计来检测它们的行程，而更完善的电机将采用某种形式的轴编码器。

商用轴编码器使用磁铁和霍尔效应传感器，或者光学传感器和编码盘。但这些可能相当昂贵，所以[Hello1024]在一个下午就拼凑出了一个替代方案。[它使用另一个电机作为编码器](https://github.com/Hello1024/brushless-encoder)，利用磁铁通过每个线圈时电感的微小变化。这种技术在便宜的电机上效果更好，因为它们的磁铁比昂贵的同类产品更不完美。

这种检测在经济上相当聪明，通过现成的电机控制器向电机发送脉冲，并测量脉冲通过驱动 MOSFET 的体二极管衰减所需的时间。在第一次使用之前，它需要一个校准程序，并且它强调整个事情仍然在测试中，但是它仍然是一个非常令人印象深刻的黑客。他上传了一个视频演示，你可以在广告下方看到。

 [https://www.youtube.com/embed/YSzVXCdpdm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YSzVXCdpdm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们在过去报道过一两个自制的编码器，在某些情况下[相当原始](http://hackaday.com/2016/06/15/wheel-of-resistors-form-unique-rotary-encoder/)但是[其他的已经更加复杂](http://hackaday.com/2014/11/01/which-way-are-we-going-concepts-behind-rotary-encoders/)。您可能还会对我们最近的[mbed](http://hackaday.com/2017/01/11/encoders-spin-us-right-round/)编码指南感兴趣。
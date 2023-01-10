# FPGA 驱动速度惊人的 LED 矩阵音频可视化器

> 原文：<https://hackaday.com/2016/06/13/fpga-powers-blazingly-fast-led-matrix-audio-visualizer/>

[萨姆·米勒]、[Sahil Gupta]和[Mashrur Mohiuddin]在康奈尔大学的 ECE 5760 项目中合作开发了一款[超快速 LED 矩阵显示器](https://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2016/sgm82_skg73_mm889/sgm82_skg73_mm889/sgm82_skg73_mm889/index.html)。

[![Real time!](img/a9c58c02718f61fe7b316c7021388be5.png)](https://hackaday.com/wp-content/uploads/2016/06/royg_bars_square_fixed.gif)

Real time!

和其他优秀的工科学生一样，他们开始寻找一种让自己生活更轻松的方法。[Sam]为另一个班级制作了一个 32×32 的 LED 矩阵。因此，他们又做了三个，最终得到了一个更大、更令人印象深刻的 64×64 LED 显示屏。

他们声称他们的动机是对音乐的热爱，但我们怀疑真正的原因是所有 EEs 都喜欢不自然的明亮的 LEDs 晚上随便看个电器，尽量不要被蒙蔽。

显示器的大脑是 Altera DE2-115 FPGA 板。代码都是纯 Verilog。FFT 和 LED 控制在 FPGA 上用硬件实现；没有 Altera 核心的东西。为了生成图像和图案，他们编写了一系列 python 脚本。但是对我们来说，真正让我们惊讶的是下面视频中的粒子测试。这种系统能够在运行中跟踪许多不同的元素并对其做出反应，为什么以大约 310 FPS 的速度扫描显示器。他们已经测试了两倍于这个速度的显示扫描，但是在黄金时间到来之前需要解决一些屏幕包裹的问题。

该团队已经承诺将所有代码上传到 GitHub，但是在成功的余波散去之前，他们可能还需要一段时间才能再次着手这个项目。休息后，您可以观看视频采访和视频中的可视化示例。

感谢他们的教授[Bruce Land]提交的提示！他的学生总是在做很酷的事情。如果你喜欢，你甚至可以在线观看他的一些精彩课程:这里有一个关于 [AVR 微控制器](https://www.youtube.com/watch?v=dT0xxaG1DhM&index=1&list=PLD7F7ED1F3505D8D5)的课程。

 [https://www.youtube.com/embed/swapwjI-fT8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/swapwjI-fT8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/z7hYsUJaWf4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z7hYsUJaWf4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/QCIetw1rhi8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QCIetw1rhi8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/5okuvNiCw8M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5okuvNiCw8M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


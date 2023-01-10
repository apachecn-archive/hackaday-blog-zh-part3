# 使用 ESP32 在示波器上观看视频

> 原文：<https://hackaday.com/2017/12/23/watch-video-on-a-oscilloscope-with-an-esp32/>

[bitluni]得到了一个全新的范围，他不能再高兴了。不，真的——查看下面的视频；他真的很开心。为了庆祝，[他用 ESP32](http://bitluni.net/oscilloscope-as-display/) 把他的望远镜变成了一个矢量显示器。

当然，在 X-Y 模式下使用示波器并不是什么新鲜事。这项技术被用来显示从 SDR 的李沙育图案到模拟计算机的 T2 弹跳球。与其说是一个实际项目，不如说是一次学习如何使用他的新工具的练习，[bitluni]的项目首先使用 ESP32 上的两个 DAC 来创建简单的李萨如模式，以了解示波器的控制。接下来，他编写了一些代码来显示 3D 点云，但是他发现原生 DAC 代码无法胜任这项工作。一点小小的改动就将速度提高了 27 倍，这对于从 I S .相机模块拍摄出色的 3D 图像和实时视频来说已经足够了。后者是通过从相机中抓取帧并以 CRT 风格逐个像素地渲染它们来实现的。结果非常清晰，关于使用示波器作为 X-Y 显示器和调整 ESP32 以获得最佳性能，还有很多东西需要学习。

需要更多关于 ESP32 的背景知识吗？从查看这些 ESP32 教程开始。

 [https://www.youtube.com/embed/T_n8PtMMLiQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T_n8PtMMLiQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


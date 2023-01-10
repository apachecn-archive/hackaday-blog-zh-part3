# 一个简单而有教育意义的无刷电机

> 原文：<https://hackaday.com/2016/04/23/a-simple-and-educational-brushless-motor/>

有时候，在理解事物如何工作时，没有什么可以替代真实的工作模型来修补。以无刷电机为例。你可能知道它们在原理上是如何工作的，但是哪些因素影响它们的运行，这些因素是如何相互作用的？受最近一些关于无刷电机的黑客帖子的启发，[Matt Venn]已经[制造了一个简单的试验板电机](http://www.mattvenn.net/2016/04/01/build-a-simple-brushless-motor/)，为好奇者研究这些设备而设计。

转子和电机主体是激光切割板层，转子设计为支持多种磁体配置。只有一个螺线管，其相对于转子上的磁体的位置可以调节。整个组件安装在试验板的边缘，可以相对于试验板旋转，以改变磁体激活驱动电路霍尔效应传感器的相位角。反过来，驱动电路可以调整其增益和时间常数，以研究它们对电机运行的影响。

[Matt]已经在他的 GitHub 库中提供了[所有的设计文件，并在休息时间下方的 YouTube 视频中记录了对电机操作的全面描述。](https://github.com/mattvenn/simple-brushless)

 [https://www.youtube.com/embed/Y1PdwugfWUE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y1PdwugfWUE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Matt Venn]在过去已经多次出现在这些页面上。无论是[他自制的货运自行车](http://hackaday.com/2014/05/16/home-made-cargo-bicycle-makes-use-of-scraps/)，他的[基于网络摄像头的家用电表](http://hackaday.com/2014/12/29/reading-power-use-data-with-a-webcam-and-python/)，还是他的[半色调 g 代码生成器](http://hackaday.com/2015/02/23/cnc-milling-photos-with-a-halftone-generator/)，他都值得一看！同时，[这是我们在 2015 年推出的无刷电机](http://hackaday.com/2015/08/20/giant-stepper-motor-gets-you-up-to-speed-on-theory/)激发了他的灵感。
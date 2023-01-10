# 零件库带来了 Arduino FM 收音机

> 原文：<https://hackaday.com/2016/12/29/parts-bin-bonanza-leads-to-arduino-fm-radio/>

在易贝搜寻零件会对你的钱包和零件箱不利。是的，储备充足是好事，但最终你会达到临界量，事情开始呈现出自己的生命。

[这种非常规的基于 Arduino 的 FM 接收器](https://www.youtube.com/watch?v=n1hPj2wfsnA)就是这样一种库存过剩的结果，尽管它可能要绕很远的路才能听到 NPR 的声音，[Kevin Darrah]的构建为其他项目提供了一些很好的提示。仍处于杂乱无章阶段，收音机以 ATmega328 为中心，通过 I C 与 TEA5767 FM 收音机模块通话。调谐由一个 10 圈游标卡尺和一个用于频率显示的模拟仪表完成。一个 15 瓦的放大器驱动一对扬声器，但[Kevin]遇到了一些放大器和调谐器模块的质量控制问题，需要额外焊接作为解决方法。下面的 longish 视频提供了一个完整的硬件和软件教程，并显示了无线电的行动。

我们喜欢这个非传统的用户界面，但使用相同的内脏更传统的调谐方法也是可能的，因为[这个复古收音机改装显示](http://hackaday.com/2015/07/02/retro-fit-old-radio-with-arduino-and-fm-module/)。

 [https://www.youtube.com/embed/n1hPj2wfsnA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n1hPj2wfsnA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


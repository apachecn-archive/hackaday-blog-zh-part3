# 复古风格的 DIY 测谎仪:信不信由你

> 原文：<https://hackaday.com/2017/01/03/retro-style-diy-polygraph-believe-it-or-not/>

测谎仪通常被称为测谎仪，但它实际上只是一台带有许多传感器的机器，在你被提问时测量心率、呼吸频率、皮肤电反应和血压等。会议可能长达三个小时，结果由受过训练的测谎仪检查人员检查，他们决定测量的反应是由于欺骗还是其他原因。现代测谎仪将数据输入计算机，计算机实时分析数据。

康奈尔大学的学生(Joyce Cao)和(Daria Efimov)决定尝试一种更为老式的测谎仪，这种测谎仪可以测量心率和呼吸率，并在一张移动的纸条和一个彩色 TFT 显示屏上记录下结果。他们也计划测量排汗量，但是没有时间。为了测量心率，电极被连接到受试者的手腕上。为了测量呼吸，他们将一个大约 3 英寸长的导电橡胶线形式的[拉伸传感器](http://hackaday.com/2016/09/16/resistance-in-motion-everything-you-should-know-about-variable-resistors/)连接到一根鞋带上，并将其缠绕在测试对象的腹部。

虽然输出没有进入计算机进行数学分析，但它会进入 PIC32 进行处理，并控制伺服系统在纸上绘制轨迹以及在 TFT 上显示。呼吸传感器和 PIC32 之间的电路相当简单，但心率电极的输出需要放大。为此，他们在另一个项目的基础上设计了一个电路，其中有一个差分放大器和两个运算放大器用于滤波。

由于部分电路连接在身体上，他们做了一些努力来防止任何触电的机会。他们使用 12 伏电压，不将测试对象连接到电源底盘接地，并首先用函数发生器测试心率电极。他们还在心率电极和放大器电路之间加入了一些电阻和电容形式的 DC 隔离电路。你可以看到这些电路，以及下面视频中的演示。心率输出看起来有点不稳定，这并不奇怪，因为身体会产生很多噪音，但呼吸轨迹看起来非常清晰。

[乔伊斯]和[达莉亚]在这个项目中得到康奈尔大学[布鲁斯·兰德]的指导，他的学生多年来产量如此之高，以至于他在 Hackaday 上有了自己的标签。从他们的项目中随机抽取一个样本，看看这个[实时视频匿名器](http://hackaday.com/2015/05/19/real-time-video-anonymizer/)，这些[跟踪乒乓球比赛的 FPGAs】，或者你也可以自己成为一名学生，](http://hackaday.com/2015/05/15/fpgas-keep-track-of-your-ping-pong-game/)[选修他的一门课程](http://hackaday.com/2015/12/21/microcontroller-lectures-by-bruce-land/)。

 [https://www.youtube.com/embed/gF0Q6B7G2Cs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gF0Q6B7G2Cs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


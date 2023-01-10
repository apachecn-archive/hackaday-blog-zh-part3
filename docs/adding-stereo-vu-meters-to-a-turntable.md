# 将立体声 VU 指示器添加到转盘

> 原文：<https://hackaday.com/2017/01/28/adding-stereo-vu-meters-to-a-turntable/>

对于过去几十年对音频设备感兴趣的人来说，一个令人高兴的发展是黑胶唱片最近重新流行起来。无论你坚持认为它们拥有更好的音质，还是你只是喜欢带有全尺寸封面和封套说明的 12 英寸磁盘的体验，你现在都可以放纵自己，让优秀的老式 LP 重新上架。

【Michael Duerinckx】是老 trance 唱片的粉丝，有一个 Ion Pure LP 唱盘，幸运的是对他来说，这不是一个无法轻易破解的独家音频设备。他所采用的技术相对简单，但却非常吸引人，[他在盘子边缘的一个环中增加了一组 LED VU 电表](http://blog.somakeit.org.uk/2014/08/13/adding-stereo-vu-meters-to-a-turntable/)。

led 背后是可靠的 LM3915，这是一种集成电路，对于任何早期生活在 20 世纪 70 年代和 80 年代音频设备中的读者来说，无疑都是熟悉的。内部是一堆比较器和一个电阻阶梯，它只需打开所需数量的输出，以匹配其输入电平。他将一对 led 放在一个带有相关 PSU 调节器的小 PCB 上，并将 led 安装在转盘边缘的 MDF 基板上钻的一排孔中。电源和音频来自转盘的电路板，其中包含一个前置放大器和 USB 音频电路。具有低电平输出的传统转盘不能直接驱动 LM3915。

这是一个相对简单的项目，转盘本身不一定是市场上最成功的，但它执行得非常干净，看起来相当漂亮。

转盘项目在 Hackaday 并不像你想象的那样常见，但是我们有一些。有[这个具体的例子](http://hackaday.com/2016/09/30/a-beautiful-turntable-with-a-heart-of-concrete/)例如，[一个非常漂亮的使用多层胶合板的例子](http://hackaday.com/2015/03/09/diy-turntable-in-a-beautiful-wooden-case/)。

南安普顿创客空间提供 [SoMakeIt。](http://www.somakeit.org.uk/)
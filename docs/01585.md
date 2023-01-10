# NES 光枪转向(视频)合成器

> 原文：<https://hackaday.com/2016/02/25/nes-light-gun-turned-video-synthesizer/>

[拉塞尔·克莱默]让我们今天很开心。我们是电子设计中极简主义的狂热粉丝，肮脏的噪音黑客，还有那把旧的 NES 轻机枪。他发布了一个[项目，将所有三个](https://hackaday.io/project/9782-nes-zapper-video-synth-theremin)结合起来，制作一个光枪控制的 VGA 视频显示器，启动时发出哔哔声。看看下面的视频吧！

要欣赏这个技巧，你真的需要[详细阅读项目日志](https://hackaday.io/project/9782/logs)。例如，从 VGA 信号创建开始。如今，最简单的方法就是用微控制器来解决这个问题。但是因为他已经这样做了，所以[Russell]后退三十年，用一个张弛振荡器和一个二进制计数器 IC 周期性地产生同步脉冲。构建的其余部分遵循这一美学选择:一切都是运算放大器和 CMOS 逻辑。例如，彩虹效果是通过发送到 R、G 和 B 声道的三级 120 度相移振荡器从音频信号中产生的。太棒了。

高层次的概述是，击中枪的传感器的光强度和位置被转换成驱动音频振荡器的电压。这个音频输出然后通过管道返回到视频发生器。观看视频，很明显，将枪指向屏幕的不同部分会改变音高，但在所有反馈都在进行的情况下，播放给定的音高几乎是不可能的。[Russell]给系统增加了更多的控制——当枪的扳机被扣下时，不管视频输入如何，它都会显示全亮度——但即使如此，我们也很难播放“玛丽有只小羊羔”。

但这不是重点。重点是可怕的，光枪挥舞嘈杂的疯狂设置为响应丰富多彩的视频背景。这已经实现了！

 [https://www.youtube.com/embed/tJvaH2gRwj8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tJvaH2gRwj8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 智能站经营娱乐，就是娱乐

> 原文：<https://hackaday.com/2017/12/11/smart-station-runs-entertainment-is-entertainment/>

这是一年中的特殊时刻——康奈尔大学[Bruce Land]嵌入式微控制器设计课程的学生项目展示时间。[Timothy]、[Dhruv]和[Shaurya]都对遥感和控制应用感兴趣，因此[他们建立了一个智能站，将视听娱乐与环境传感结合起来](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2017/tmb233_dg566_sl2462/tmb233_dg566_sl2462/tmb233_dg566_sl2462/index.html)。

与本课程中的其他项目一样，智能站建立在 PIC32 开发板上。它通过 RN-52 模块进行蓝牙音频播放，并在 3D 打印的外壳顶部安装了一个新像素环形式的节拍匹配灯光秀。但是那些闪光灯不仅仅是为了派对。它们还提供关于环境的视觉反馈，这些反馈来自麦克风、加速度计、温度和湿度传感器以及亮度传感器的用户可调高低触发值。

该小组希望增加一个超声波唤醒功能，但它拒绝使用 PIC 的 3.3V。NeoPixel 戒指也想要 5V，但没那么挑剔。它在 3.3V 时看起来非常亮。另一个挑战来自 I C、UART、模拟输入和数字输出的组合。他们不得不去芯片的勘误表验证它，但它是存在的:每当我 C1 被启用，前两个模拟引脚受到损害，而且没有官方的解决方案。该团队通过使用一个模拟引脚和一个多路复用器解决了这个问题。休息之后你可以看看那些闪光灯。

也许你更喜欢在木头里工作。如果是这样，[你可能会喜欢这个六边形的视听效果](https://hackaday.com/2016/12/25/bluetooth-speaker-with-neopixel-visual-display/)。

 [https://www.youtube.com/embed/CUuWdApINUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CUuWdApINUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


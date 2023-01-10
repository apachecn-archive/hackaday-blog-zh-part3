# 将吉他合成引入微控制器

> 原文：<https://hackaday.com/2018/04/10/bringing-guitar-synthesis-to-the-microcontroller/>

如果您在嵌入式环境中处理音频，多年来最好的选择是 Teensy 3 微控制器板。这一选择主要是因为它令人难以置信的功能和音频库，但直到现在我们还没有看到一个踏脚转盘风格的界面将 Teensy 发挥到了极致。现在，在[【wolk stein】的 GitSynth](https://github.com/wolkstein/GitSynth127) 中，我们拥有了合成器处理电吉他信号所需的一切。

这个版本的核心是一个小小的 3，以及随之而来的所有音频好东西。还包括一个 USB MIDI 和音频接口，它们都巧妙地连接到踏脚转盘背面的面板安装 USB-B 连接器上。其他控制包括一个用于吉他和合成器的单声道输入插孔，两个用于立体声输出的单声道输出插孔，一组用于旁路、拍子速度、预设选择的脚踏开关，一个用于表情踏板的插孔，以及一些在 LCD 用户界面上移动的按钮。

虽然在踏脚转盘中放置一个强大的微控制器是一个我们已经见过很多次的项目，但这个项目真正闪耀的是为具有真正显示器和鼠标的设备构建的 MIDI GUI。[Wolkstein]为这个合成器开发了一个基于 PyQt 的应用程序，它有大量的按钮和滑块，看起来足够类似于一个真正的合成器。这里有足够的可配置性给任何人。

你可以看看下面的演示视频(德语，但有自动翻译字幕)。

感谢[Mynaru]的提示！

 [https://www.youtube.com/embed/Vln2Wjr82cE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Vln2Wjr82cE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


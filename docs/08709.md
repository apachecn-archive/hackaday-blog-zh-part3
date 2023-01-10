# 只有机械继电器可以自动切换高保真音源

> 原文：<https://hackaday.com/2018/03/10/only-mechanical-relays-will-do-for-automated-hi-fi-audio-source-switching/>

如果你是高保真质量模拟高保真音响的狂热爱好者，那么通过固态设备根本无法实现信号源之间的切换。只有物理开关才行得通，因为它们没有硅等效物可能带来的额外噪声或失真的风险。

这就是[Skrodahl]基于[继电器的音频切换板](https://hackaday.io/project/46280-muffsy-stereo-relay-input-selector)背后的理念，它拥有 5 个高质量的继电器，每个继电器处理一个立体声输入，它们的控制要么传递给一个旋转开关，要么传递给一个 ESP32 模块。音频侧和开关侧的接地连接相互隔离，以避免瞬态噪声进入扬声器。

你可能会认为音频切换板确实是一个非常简单的设备，因此不值得 Hackaday 关注，但像这样的模块很容易搞得一团糟，他们已经做出了一些努力来避免陷阱。开关晶体管的金属罐版本似乎有点矫枉过正，但花哨的音频是一个有趣的业务。

如果 ESP 不是你的囊中之物，我们在过去为你带来了另一个基于继电器的音频切换器[，它使用了 Atmel 芯片](https://hackaday.com/2011/12/09/tiny-audio-switcher-eliminates-repetitive-plug-swapping/)。
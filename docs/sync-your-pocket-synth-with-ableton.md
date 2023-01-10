# 同步你的袖珍合成器与 Ableton

> 原文：<https://hackaday.com/2017/02/05/sync-your-pocket-synth-with-ableton/>

青少年工程袖珍操作器是非常受欢迎的设备——袖珍合成器，充满了令人兴奋的声音和节奏选项。它们也非常实惠。然而，这是有代价的——它们不具备 MIDI 连接功能，因此很难将它们集成到更大的数字音乐系统中。别害怕，小天平会支持你的。[这个 Max 补丁可以让你同步 Ableton Link 网络到你的口袋运营商](http://little-scale.blogspot.com.au/2017/01/audio-pulse-link-sync.html)。

little-scale 的商标是尽可能使用廉价的现成硬件来创建有用的软件和硬件设备。这里的小窍门是一个简单的 Max 补丁与一个 2 美元的 USB 声卡或蓝牙音频适配器相结合。一切都很简单:袖珍操作器有各种同步模式，它们在音频脉冲上同步，本质上是一个点击轨道。他们在车上使用 3.5 毫米立体声插孔，通常使用一个通道接收合成器的音频，一个通道接收同步脉冲。在 Ableton 中合成合适的同步脉冲，然后通过蓝牙或 USB 音频输出将它们输出给 Pocket Operators，这是一项简单的工作。

袖珍操作器以 2 PPQN 的速率同步，即每个四分音符一个脉冲。little-scale 表示，KORG volcas & monotrons 也应该可以与这个补丁一起工作，因为它们以相同的速度运行，但目前尚未测试。如果你碰巧自己尝试了这个，让我们知道它是否对你有用。休息下的视频。

我们以前在 Hackaday 上见过 pocket synths，这款[有吸引力的混音器是为 KORG Volcas](http://hackaday.com/2014/11/30/mixer-for-korg-volcas/) 设计的。

 [https://www.youtube.com/embed/iVnAqroo62k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iVnAqroo62k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


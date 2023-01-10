# 声学手风琴变成 MIDI 哦，太复杂了！

> 原文：<https://hackaday.com/2017/02/01/converting-an-acoustic-accordion-to-midi-oh-the-complexity/>

每个人都知道手风琴很酷——它们看起来像苍蝇，发出整齐的声音，让你的浪漫兴趣变得火热和不安。不酷的东西只被归入声学范畴。你怎么能在一个拥挤的体育场打球，或者像那样铺设一条水晶般透明的跑道？你可以出去买一个电动手风琴，但即使是低端型号也有很高的价格。但是，这是黑客日，你知道我们将告诉你一个发现更好方法的人。

更好的方法，在 Brendan Vavra 的一个构建中展示，是[拿一个原声手风琴，把它转换成 MIDI](http://imgur.com/a/U7L83) 。他建造的基础是在易贝花 150 美元买的一架像样的全尺寸原声手风琴。总的来说，它处于良好的机械状态，但一些簧片跑调或根本不起作用。幸运的是，这并不重要，因为他无论如何也不会使用它们。不要被下面的演示视频忽悠了；这听起来像是他在演奏原声乐器，但是请注意，他没有在拉风箱！然而，风箱也不是无用的，因为它可以作为 MIDI 输入反馈数据。

[Brendan]的建造计划要求将 Arduino Mega 与一系列光电中断器相连，这些光电中断器将检测按钮按压并发出 MIDI 信号。但是，首先他必须把这个东西拆开——考虑到仪器的复杂性，这可不是一个小任务。手风琴有 120 个按钮，它们是不可互换的，这意味着他必须在拆卸时仔细记录它们。

 [https://www.youtube.com/embed/s197ojk8npI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/s197ojk8npI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



值得注意的是，他在没有任何重大障碍的情况下完成了这件事(只是花了很多时间)。安装了光电中断器，所有的电子设备都很好地塞进了手风琴的主体。首先，[Brendan]用 Arduino 的 USB 电缆将它连接到他的计算机上，以证明这个概念。工作之后，他升级了蓝牙传输信号的设置，甚至增加了一个气压传感器，允许他使用风箱来表达和改变音量。尽管我们在之前已经看到了[精心制作的 MIDI 版本，但这可能只是在一个小的包中为复杂性取了蛋糕。哦，而且非常酷。](http://hackaday.com/2016/11/09/a-pipe-organ-for-the-midi-generation/)

[via [r/somethingimade](https://www.reddit.com/r/somethingimade/comments/5phlkp/i_turned_an_acoustic_accordion_into_a_midi/)
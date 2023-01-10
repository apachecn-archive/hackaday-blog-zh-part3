# 一部分是烙铁，一部分是手持示波器

> 原文：<https://hackaday.com/2017/09/28/part-soldering-iron-part-hand-held-oscilloscope/>

如果你想在市场上买到温控烙铁，目前一个有吸引力的选择是从中国邮购的 TS-100 烙铁。这是一个多功能熨斗，手柄内置数字温度控制器，配有一个微型有机发光二极管显示器。它是轻量级的，质量合理，它的所有设计和软件都是可用的，并被称为开源(尽管当我们审查它时，我们找不到伴随代码的开源许可证。)这种结合导致它成为一种流行的选择，并出现了相当多的软件黑客。

我们最近读到的一本书可能被最好地描述为来自天才和疯狂之间的界面，无意贬低其作者令人印象深刻的成就。[Befinitiv] [在 TS-100](https://befinitiv.wordpress.com/2017/09/26/ts100-oscilloscope-hack/) 上实现了一个工作示波器，它使用烙铁尖作为探头，有机发光二极管作为显示器。它需要对硬件进行小的修改，以将铁触点引入微控制器的 ADC 引脚，目前没有输入保护，因此铁很容易被烧坏，但它可以工作。

文章中强烈建议，这不是一件可以投入生产的作品，你不应该把它放在熨斗上。至少，没有输入保护和电阻分压器是不行。但尽管如此，它仍然是一件令人印象深刻的作品，一个工作的烙铁，成为一个菜单选择的范围。让我们来看看“铁镜”的工作情况，我们在休息时发布了一段视频。

 [https://www.youtube.com/embed/Gg9mKVMbp0I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Gg9mKVMbp0I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你对铁很好奇，[你可以看看我们的 TS-100 评测](https://hackaday.com/2017/07/24/review-ts100-soldering-iron/)。或者，如果你有一个和一个范围听起来太冒险，[把俄罗斯方块放在你的铁](https://hackaday.com/2017/07/07/tetris-on-a-soldering-iron/)怎么样？
# SDRAM 逻辑分析仪使用 AVR 和肮脏的伎俩

> 原文：<https://hackaday.com/2016/03/15/sdram-logic-analyzer-uses-an-avr-and-a-dirty-trick/>

我们经常看到“逻辑分析仪”项目，它只不过是微控制器尽可能快地读取数据，将其发送到 PC，然后绘制结果。根据微控制器的速度，这些项目从足够到不太有用不等。

乍一看，[【秘传的】逻辑分析仪项目](https://hackaday.io/project/4159-sdramthing45-logic-analyzer)里面有一个 AVR，所以应该是低端的。然后你看看规格:32 个通道，每秒 30 兆样本。里面有 AVR 怎么工作？

答案在于元器件的选择。分析仪使用 128MB SDRAM DIMM(就像旧电脑可能使用的主内存)。那是有道理的；Arduino 无法在内部存储太多数据。然而，存储容量并不是这一选择的关键。看来[秘传]有办法让 RAM“自由运行”。

想法是使用 Arduino(或其他主机微控制器)来设置内存。存储器的一些输出位反馈到地址和数据线。然后，微控制器靠边站，SDRAM 以存储器的主要时钟速率自行将样本时钟输入存储器。

当然，这对于复杂的触发这样的事情来说并不好，而且你把一些内存存储让给了控制“程序”(如果这个词没错的话)。然而，很容易看出这种技术在其他情况下也很有用，在这些情况下，您希望卸载 CPU 来进行重复的数据传输。比如【秘传】也曾经用这种方法驱动过[一个液晶面板](https://sites.google.com/site/geekattempts/home-1/sdramthing)。

为了证明这一点，下面的视频显示，即使在移除 AVR 微控制器后，该设备仍能工作。只有在安装阶段才有必要。诚然，逻辑分析仪部分并不酷。如果你想要一个逻辑分析仪，从 Hackaday 商店或者其他便宜的商店买一个。如果你想在[推出自己的](http://hackaday.com/2015/02/19/turn-your-beagleboneblack-in-to-a-14-channel-100msps-logic-analyzer/)，也有很多选择。

但对于纯粹的大胆和肮脏的诡计，你不得不佩服这个设计如何以独特的方式使用 SDRAM。这让你想知道我们还能以什么奇怪的方式使用其他组件。

 [https://www.youtube.com/embed/uXlbCuw5VU0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uXlbCuw5VU0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


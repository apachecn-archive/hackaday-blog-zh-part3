# 袖珍木管乐器 MIDI 控制器帮助你携带一首曲子

> 原文：<https://hackaday.com/2017/11/13/pocket-woodwind-midi-controller-helps-you-carry-a-tune/>

很容易对音乐着迷，尤其是一旦开始演奏。你想去哪都做音乐，完全不切实际。不相信我？看看你能在地铁上吹口哨或在公交车上击鼓多长时间，然后你的乘客就会反抗。还有一个更好的方法，那就是便携式 USB MIDI 控制器。

[Johan]想要一个口袋大小的木管乐器 MIDI 控制器，但他发现所有现有的控制器都太大太笨重，无法随身携带。他用一个小小的 Teensy 和一个压力传感器创造了 TeensieWI。它使用内置的 cap sense 库从铜带键读取输入，生成 MIDI 消息，并通过 USB 或 DIN 发送它们。背面的另一对导电垫允许八度变化。[Johan]后来添加了一个 PSP 操纵杆来进行弯音、调制和滑行。这是一个简单的建立，创造了一个多功能的文书。

你实际上并没有把空气吹进吹口——只是让它从你的嘴的两侧逸出。如果你已经发展了一种口型，这可能需要一些时间来适应。这些数值由压力传感器[决定，压力传感器](https://www.digikey.com/product-detail/en/nxp-usa-inc/MPX5010GP/MPX5010GP-ND/464055)使用压阻来计算你吹气的力度。可以在设置中配置默认的呼吸响应值。

TeensiWI 应该很容易复制或混合到任何合适的机箱中，尽管紫外线反应丙烯酸树脂看起来非常棒。[Johan]关于 IO 的文档是一流的，包括一个带有指法图的用户指南。对于那些拿走我钱的人，[[Johan]出售他们准备在 Tindie](https://www.tindie.com/products/yoe/twi-a-teensy-based-usb-midi-woodwind-controller/)上摇滚。休息之后，请观看简短的演示剪辑。

几年前，我们看到了一个木管乐器 MIDI 控制器，它最终配备了一个板载合成器。想建一个 MIDI 控制器？，[就像这个漂亮的建筑，它使用硬盘作为滚轮](https://hackaday.com/2015/11/09/two-turntables-and-no-microphone/)。

 [https://www.youtube.com/embed/G5NCUiZrPEE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G5NCUiZrPEE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/EOcJjs17dhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EOcJjs17dhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


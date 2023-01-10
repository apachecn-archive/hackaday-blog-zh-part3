# 便携式蓝牙扬声器对声音有反应

> 原文：<https://hackaday.com/2017/05/01/portable-bluetooth-speaker-reacts-to-sound/>

[IanMeyer123]应该在做他的高级设计项目。相反，他[创造了一个声音反应蓝牙扬声器](http://imgur.com/gallery/9iIrI)，这可能不会让他获得 A 级，但至少会让团队开心。

[Ian]从放大器和电源开始。该放大器是基于流行的 TDA7297 芯片的 15 瓦、12 伏型号。电源来自额定功率为 185 瓦时的便携式笔记本电脑电池。[伊恩]自己说，这对于这个项目来说是绝对的矫枉过正。虽然[伊恩]还没有对他的设置运行任何寿命测试，我们猜测它将在几天内评级。

每个蓝牙音箱都需要一场甜蜜的灯光秀吧？[Ian]用 Adafriut 的 Neopixel 戒指包裹他的 2 英寸全频扬声器。WS2812 由 Arduino 驱动。当音乐播放时，MSGEQ7 允许 Arduino 按照节拍播放灯光表演。当立体声关闭时，DS3231 实时时钟模块允许 Arduino 在两个铃声上显示时间。如果你对这个项目的代码感兴趣，[Ian] [在他的 Reddit 帖子](https://www.reddit.com/r/DIY/comments/66u05d/soundreactive_portable_bluetooth_stereo/)上发布了它。Reddit 并不是一个很好的代码库，所以请[Ian]建立一个 GitHub 账户，或者把你的项目放到 [Hackaday.io](https://hackaday.io) 上！

[Ian]没有意识到有多少电线会在扬声器里飞来飞去。这可能是为什么线路看起来有点可怕。所有的混乱都被藏在一个建造良好的木箱下面。

如果你想看另一个采用新像素显示屏的蓝牙扬声器，[点击这里](http://hackaday.com/2016/12/25/bluetooth-speaker-with-neopixel-visual-display/)查看【Peter 的】项目。对更多便携式电源装置感兴趣？[这是给你的](http://hackaday.com/2013/08/13/the-batbox-portable-power-polished-and-professional-plus-smoke/)！

 [https://www.youtube.com/embed/mFmnycyw4w4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mFmnycyw4w4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


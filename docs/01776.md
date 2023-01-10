# 红外线特雷门琴

> 原文：<https://hackaday.com/2016/03/21/the-infrared-theremin/>

传统的特雷门琴或多或少是一个带有两根金属棒的音频振荡器。使用近程传感，一个杆控制振荡器的音高，另一个控制音量。[Teodor Costachiou]显然问了自己一个非常好的问题:为什么接近传感器必须使用电容？结果是基于 Arduino 的 theremin 使用红外传感器来确定手的位置。

[Teodor]使用了一种特殊类型的 Arduino——翻转和点击——因为他想将点击板用于红外传感器，并通过基于 VS1053 的 MP3 板生成声音。诀窍是 VS1053 有一个实时 MIDI 模式，这就是特雷门琴如何使它发出音调。

当然，真正的特雷门琴显然是模拟的。手位置的微小变化会引起输出的微小变化。随着数字传感器和声音的产生，输出更加离散，但根据[特奥多尔]的说法，效果还不错。我们希望有一个视频(或者至少是一个音频片段)，但是(特奥多尔)辩解说他不是音乐家。他在帖子里附上了一段真实的特雷门琴表演视频，你可以在下面看到。但那是真正的模拟特雷门琴。

如果你想做一些更传统的东西，看看[打开特雷门](http://hackaday.com/2016/01/24/finally-a-modern-theremin/)。或者，如果你想锻炼身体，试试萜品酮怎么样。如果你这样做，并可以播放主题为*地球停转之日*，我们很乐意看到视频。与此同时，如果你不知道特雷门有间谍联系，你就不会关注[的黑客帖子。](http://hackaday.com/2015/12/08/theremins-bug/)

 [https://www.youtube.com/embed/K6KbEnGnymk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K6KbEnGnymk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


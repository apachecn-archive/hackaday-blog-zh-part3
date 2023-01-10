# 谈论星际旅行

> 原文：<https://hackaday.com/2016/06/08/talking-star-trek/>

语音生成和识别已经有了很大的发展。就在不久前，我们还在一家早餐店里，忍受了 30 分钟一个十几岁的女孩尖叫着“打电话给贾斯汀·泰勒！”反复打她的电话，没有结果。现在电话语音已经足够好了，除非你想要隐私，否则你可能永远不会使用键盘。每次我们问谷歌或 Siri 一个问题并得到答案，都会让我们觉得自己生活在《星际迷航》中。

[Smcameron]大概也这么觉得。一段时间以来，他一直致力于一个受《星际迷航》启发的名为“太空书呆子”的桥梁模拟器。他决定通过添加语音命令和响应来测试 Linux 语音支持的当前状态。你可以在下面的视频中看到结果。

对于语音输出，他使用了 pico2wave 和 espeak。也有节日，但他不能让那个工作。他还将 PocketSphinx 用于语音识别，并提供了如何对系统进行单词预训练以使其更好地响应的信息。在视频中，你可以看到它并不完美，但它相当不错。

等式的另一部分是识别自然语言，[Smcameron]也讨论了这一点。如果这是一艘真正的星际飞船，你可能需要在用户界面上做一些工作，以确保在采取一些激烈的行动之前，你听到了正确的事情(“我说:‘启动曲速引擎’，而不是‘启动曲速五’！”).

如果你的系统不如一个完整的 Linux 系统强大，考虑一下 Arduino 的 uSpeech。你也可以去看看[贾斯帕](http://hackaday.com/2014/06/07/how-to-upgrade-jaspers-voice-recognition-with-atts-speech-to-text-api/)。

 [https://www.youtube.com/embed/tfcme7maygw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tfcme7maygw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 你说，你的范围服从

> 原文：<https://hackaday.com/2016/03/29/you-speak-your-scope-obeys/>

我们一直在为各种各样的语音识别解决方案绞尽脑汁。你真正想用它做什么？不起床就关掉卧室的灯？当然，它有一些 2001:太空漫游~~耀斑~~的天赋，但坦率地说，我们已经有了一个遥控器。在我们看来，声音控制的最佳理由是在你的手或眼睛已经忙碌的时候控制一些东西。

[Patrick Sébastien Coulombe]显然双手都放在示波器探头上。这就是他开发 Speech2SCPI 的原因，speech 2s CPI 是语音识别和示波器控制协议的快速混合。它结合了 [Julius 开源语音识别器项目](https://osdn.jp/projects/julius/)和[可编程仪器标准命令(SCPI)](https://en.wikipedia.org/wiki/Standard_Commands_for_Programmable_Instruments) 语法，让他的范围服从他的每一个命令。你得看看休息时间下面的视频，才能相信它有多有效。它甚至能处理他的法国口音。

更好的是，这一切都在他的电脑上完成，而不需要将数据发送到云端，因此他可以定制系统以满足自己的需求。(Julius 系统利用已知的语法和有限的一组单词来提高其准确性。)【Patrick】的设置*使用亚马逊服务进行可选的文本到语音的响应，但如果你愿意，可以很容易地用 [Festival](http://www.cstr.ed.ac.uk/projects/festival/) 或任何其他开放的文本到语音引擎来代替。一切都是用 Python 写的，并且体面地记录在[Patrick]的[GitHub 上。](https://github.com/patricksebastien/speech2scpi)*

 *我们熟悉亚马逊、谷歌和苹果的语音识别应用，但我们是开放开发的忠实粉丝。所以向[帕特里克]脱帽致敬，因为他利用了朱利叶斯。我们完全同意他的观点，把这一切放在一个专用的树莓派上会很棒。但是像示波器控制装置这样有限的词汇，我们不禁想知道是否有可能在更小的微控制器上完成这样的事情？

 [https://www.youtube.com/embed/KRjL55Ug-5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KRjL55Ug-5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

*
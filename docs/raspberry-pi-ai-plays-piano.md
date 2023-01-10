# 树莓皮艾弹钢琴

> 原文：<https://hackaday.com/2017/09/06/raspberry-pi-ai-plays-piano/>

[Zack]看了[Dan Tepfer]用带 MIDI 键盘的电脑在演奏时做一些自动填充的视频。他决定要做得更好，并着手创造一个人工智能，它将实时学习如何在人类表演的间隙插入适合风格的曲调。

如果你想要代码，可以在 [GitHub](https://github.com/schollz/PIanoAI) 上找到。然而，真正有趣的部分是[关于他的经历、成功和失败的日志](https://rpiai.com/piano/)。如果你想看看结果，看看下面的视频，他重复了大约 30 秒，当表演者停止时，人工智能开始接管旋律。

最初的版本用 Python，后来的版本用 Go。[Zack]使用了一些不同的算法，从简单的人类玩家的回声到基于先前的笔记开发马尔可夫链。最初的结果不是很好——有早期试验的视频。部分问题是 Python 实现很慢，但是 Go 版本执行得更好。

[扎克]也尝试了神经网络。然而，结果也不尽如人意。最后，他选定了一种基于自己打法的修正马尔可夫链算法。

我们很乐意看到这个人工智能与右侧的[致动器](https://hackaday.com/2017/03/14/arpeggio-the-piano-superdroid/)匹配。或者也许应该把[做成一架钢琴](https://hackaday.com/2015/09/06/its-an-upright-piano-its-a-looper-its-a-pi-project/)。

 [https://www.youtube.com/embed/vF0uQax56a4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vF0uQax56a4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


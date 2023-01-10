# 使用光滑板的 3D 激光雕刻

> 原文：<https://hackaday.com/2016/03/04/3d-laser-carving-with-the-smoothieboard/>

昂贵的激光切割机具有 3D 雕刻模式，在蚀刻设计时改变激光功率，以创造 3D 效果。[本杰明·奥尔德逊]认为这可以在廉价的中国激光器上复制——所以他开发了自己的程序，名为[smooth curve。](http://www.non-newtonian.com/uncategorized/smoothcarve/)

他有一个非常便宜的蓝盒 40W 二氧化碳激光器，你可以花 600-800 美元从易贝那里买到，但他用一块光滑的板代替了控制板，作为一个简单的升级。他在 MatLab 中编写了程序来分析灰度图像，然后给不同的灰度分配能量等级。你可以在他的 GitHub 上看到这个软件并亲自试用。

生成的应用程序非常方便——休息之后，看看它雕刻出的 Jolly ~~Rancher~~ 扳手！

 [https://www.youtube.com/embed/S6XyUa0RD-k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S6XyUa0RD-k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你不知道的话， [SmoothieBoard 是最重要、最终极的 CNC 控制器](http://hackaday.com/2013/09/30/smoothieboard-the-be-all-end-all-cnc-controller/)——自从它在 Kickstarter 上发布以来，已经有三年的历史了！
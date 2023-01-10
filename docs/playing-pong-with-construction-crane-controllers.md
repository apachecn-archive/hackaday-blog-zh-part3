# 用建筑起重机控制器玩乒乓？

> 原文：<https://hackaday.com/2015/09/20/playing-pong-with-construction-crane-controllers/>

这是一个会让你挠头的项目！有没有想过使用那些大型重型车间起重机控制器来玩乒乓球会是什么样子？没有吗？我们也没有，但这并没有阻止[hwhardsoft]尝试它！

现在公平地说，他们实际上是为制造他们的公司建造的——猜猜这可能是一个在大厅里的有趣游戏？该项目的核心是一个 Raspberry Pi 2 和一个用 Python 编写的 Pong 游戏。有趣的部分是连接控制器。

每个控制器都是无线的，有一个单独的控制盒，所以他们能够修改控制盒，以避免对实际控制器进行任何更改。但由于他们想使用操纵杆，他们仍然必须使用额外的 ATMEG328 微控制器来执行 Pi 的模数转换，这并不完全是即插即用。

 [https://www.youtube.com/embed/j92sWwhzWk0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j92sWwhzWk0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



总的来说，这个系统看起来工作得很好，对于任何大厅/销售办公室来说都是一个非常可爱的功能！

我们最喜欢的乒乓球游戏[就是这个游戏](http://hackaday.com/2014/12/08/crosswalk-pong-auf-deutschland/)——它太有意义了！
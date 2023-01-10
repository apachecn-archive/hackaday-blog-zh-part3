# x 标记时钟

> 原文：<https://hackaday.com/2017/01/12/x-marks-the-clock/>

基于 Arduino 的时钟并不短缺。尽管如此，[菲德先生的]时钟还是得到了第二次审视，因为它看起来非常独特。然后再看第三遍，因为外行人很难读懂。

时钟使用三个由发光二极管制成的 x。一个 X 代表小时(这是 24 小时制)，另一个代表分钟，还有一个代表秒钟。每个 X 的左边代表数字的十位数，而右边是单位。

但是等等…即使 X 的两边各有两段，那也只允许从 0 到 3 的二进制数，对吗？[Mr_fid]使用另一个维度——颜色——来绕过这个限制。尽管他称之为二进制时钟，但更准确地说是二进制编码十进制(BCD)时钟。红色发光二极管代表数字一到三。绿色发光二极管是四至六个。两条蓝色线段代表 7 到 9。这听起来很复杂，但如果你看了下面的视频，就会明白了。

这不是[菲德先生]的第一只钟。他使用 DS1307 实时时钟模块来弥补 Arduino 的漂移趋势。即使你对时钟不感兴趣，用塑料安装 LEDs 以及他将它们彼此隔离的问题——可能会在其他显示器中派上用场。

这些年来，我们已经看到了很多 Arduino 时钟，包括一些会说话的。我们甚至看到了一些被称为[互动家具](http://hackaday.com/2016/10/17/its-a-clock-its-a-puzzle-its-the-gooniebox/)的产品，不管那是什么。

 [https://www.youtube.com/embed/1xDsjSiDVL8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1xDsjSiDVL8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


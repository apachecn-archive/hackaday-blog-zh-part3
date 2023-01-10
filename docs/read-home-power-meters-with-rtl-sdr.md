# 用 RTL-SDR 读取家用电表

> 原文：<https://hackaday.com/2017/12/21/read-home-power-meters-with-rtl-sdr/>

[k-roy]讨厌电。尤其是一不小心就会致命的那种。受大众感知家用能源监控器(必须由电工安装在主断路器盒中)广告的困扰，[k-roy]开始寻找一种更便宜、更简单的方法。他想知道电力公司是如何监控他的电表的，并且猜对了，它一定是在无线传输信息。也许他可以偷听？

使用一个便宜的 RTL-SDR，没多久[k-roy]就接入了这个传输，并使用一个简单的命令偶然发现了他整个邻居的功率读数:

`~/gocode/bin/rtlamr -msgtype=idm --format=json -msgtype=scm+`

具有讽刺意味的是，最难的部分并不是窥探附近每个人的电力和用水模式，而是试图找出哪个水表是他的。最后，他能够用 PHP 制作一些漂亮的数据图形布局。

在我们这个时代，我们已经见过一些[正义的电表黑客](https://hackaday.com/2016/07/11/put-a-reverse-engineered-power-meter-in-your-toolkit/)，但这一个因其简单和优雅而脱颖而出。请务必查看[k-roy 的]博客以了解更多细节，并查看[rtlamr 的] [github](https://github.com/bemasher/rtlamr) 以了解用于读取电表的程序。

感谢[Jasper J]的提示！
# 我们宣布口袋妖怪 Go GPS 大师作弊

> 原文：<https://hackaday.com/2016/07/26/we-declare-the-grandmaster-of-pokemon-go-gps-cheats/>

自从 Pokemon Go 在几周前风靡世界以来，我们一直试图抓住他们。不是口袋妖怪；我们一直试图收集所有的硬件黑客，特别是最完整的 GPS 欺骗黑客。我们现在准备宣布[为口袋妖怪 Go](https://www.youtube.com/watch?v=9mC71c6zRUE) 的第一个特级大师 GPS 欺骗黑客。它向你的手机广播虚假的 GPS 信号，允许玩家使用游戏操纵杆在真实世界中“漫步”。

在我们看来，这一切都是对的。他们正在发射无线电信号，并通过使用包含 GPS 天线的 RF 屏蔽盒来做负责任的事情。硬件设置意味着将手机放入内部，连接信号发生器和 GPS 评估硬件。然后，谷歌地球成为导航界面——操纵杆允许玩家实时移动，坐标被转换为 GPS 信号，在盒子内部传输。

现在，我们确实说了“刚刚好”。首先，当你打开盖子时，射频屏蔽盒不会阻止你的假 GPS 信号(这样他们就可以接触到手机的触摸屏)。对于原型版本来说，这可能是可以原谅的，但加速度计数据是一个更大的问号。

当我们查看之前《口袋妖怪 Go》的[基于 SDR 的射频欺骗](http://hackaday.com/2016/07/19/pokemon-go-cheat-fools-gps-with-software-defined-radio/)和 [Xcode GPS 欺骗](http://hackaday.com/2016/07/19/pokemon-go-gps-cheat-if-you-dont-fear-getting-banned/)时，有许多人发表评论说，负责《口袋妖怪 Go》的开发人员 Niantic 最终会意识到你在作弊，因为加速度计数据与 GPS 移动量不匹配。你怎么想呢?这个应用程序是否足够复杂，能够识别这种类型的射频黑客攻击？

 [https://www.youtube.com/embed/9mC71c6zRUE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9mC71c6zRUE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[/r/电子](https://www.reddit.com/r/electronics/comments/4unzp2/cheating_in_pok%C3%A9mon_go_using_a_signal_generator/)
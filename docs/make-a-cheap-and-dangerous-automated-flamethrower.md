# 做一个便宜(而且危险)的自动喷火器

> 原文：<https://hackaday.com/2015/10/16/make-a-cheap-and-dangerous-automated-flamethrower/>

没有什么比火焰喷射器的快速喷射更能照亮夜晚，但你不能在塔吉特百货的万圣节装饰通道里买到它们是有原因的。由于显而易见的原因，它们是危险的。[Erco]似乎对死亡没有特别的恐惧，他展示了如何用一根小蜡烛、一个伺服系统、Arduino 和一罐发胶来制作一个简单的喷火器。特别是 Tresemme 的超强握持力，尽管我们认为确切的类型并不那么重要。他所做的只是在发胶前安装蜡烛，然后安装伺服系统，这样[手臂会将喷头向下压](https://www.youtube.com/watch?v=mHKNzyjM228)。蜡烛完成剩下的工作，点燃发胶中高度易燃的推进剂，产生火焰喷射器的效果。[欧科]正在使用其中的四个，它们配合音乐同步发射。

这个似乎有点冒险。伺服系统有锁定的习惯，没有什么可以阻止它们锁定在打开位置，或者在 Arduino 崩溃时卡在那里。当电源被移除时回复到关闭位置的继电器或其他开关在这里会更合适。其次，没有紧急关闭开关。[Erco]已经把 Arduino 连在喷火器旁边了，所以你得伸手把它断开。这已经够冒险的了，但他还尝试了一种在出现问题时无法禁用的 [4 向配置](https://www.youtube.com/watch?v=FIKK_1dE7Vo)(如随附图片所示)。第三，发胶罐和明火之间没有防火保护，所以如果喷头受热熔化或失效，游戏就结束了。最后(也是最重要的)，灭火器在哪里？我们想听听你如何在考虑安全的情况下建造它。请在下面的评论中告诉我们。

我们是火焰和爆炸的超级粉丝:我们看过几场生存研究实验室的表演，被它们毁灭性的烟火震撼了。但是，正如 SRL 负责人[马克·波林在最近的一次谈话](https://youtu.be/UlWEI-zYLjQ?t=208)中所说，“当事情在 SRL 展会上发生时，那是故意的”。

 [https://www.youtube.com/embed/FIKK_1dE7Vo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FIKK_1dE7Vo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


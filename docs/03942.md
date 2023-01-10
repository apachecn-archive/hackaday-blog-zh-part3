# ESD 对我的电路有什么影响，我该如何防范？

> 原文：<https://hackaday.com/2016/10/25/what-does-esd-do-to-my-circuit-and-how-can-i-protect-against-it/>

[Kevin Darrah]正冒着食指紧张的风险学习 ESD 保护。他穿着一双白袜子，一张超细纤维沙发和一张尼龙地毯，就像书中的巫师一样，从自己的双手中召唤出电流(在屋子里拖着脚走了一圈之后)。他的精力集中在一个牺牲性的 2N7000 小信号 MOSFET 上。

当你电击一个电路时会发生什么？它会不会像电影中那样瞬间死亡:浓烟滚滚涌向屋顶，远处警笛大作？[凯文]建立一个简单的电路来展示真相。它有一个按钮，一个 MOSFET，一个 LED，和一些维生素。当你按下按钮时，灯就灭了。

他稍微移动了一下，然后用一个小霹雳电击了 MOSFET。放电后，MOSFET 不会一直关灯。令人震惊的发展。

那么，一个人如何防止这些暗能量破坏电路呢？任何一个有沃尔玛礼品卡的人都可以召唤的能量？有人如何压制这种邪恶？

[Kevin]向我们展示了如何使用两个二极管和一个电阻来分流静电放电产生的高电压，使其远离敏感元件。他还实验性地验证和解释了每一个的目的。电阻本身没有任何作用，它是用来保护二极管的。二极管是用来保护 MOSFET 的。

最后，他有了一个电路，可以承受最剧烈的拖曳，棉袜摩擦尼龙地毯，穿过他的地板。它可以承受强大的电荷，只有一个成年男子跳在他的沙发上才能召唤。确实是强大的魔法。休息后的视频。

 [https://www.youtube.com/embed/GshgZE5ANQ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GshgZE5ANQ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


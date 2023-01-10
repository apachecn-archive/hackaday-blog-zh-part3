# 没有勺子；自动自搅拌马克杯

> 原文：<https://hackaday.com/2016/01/24/there-is-no-spoon-automatic-self-stirring-mug/>

有时候意识到没有勺子这个事实是有帮助的。至少，不是用【c 罗】的[自动自搅拌马克杯](https://hackaday.io/project/9107-automatic-self-stirring-mug)。起初，它只是杯子底部的一个小推进器，通过按下手柄上的按钮来启动，但这并不像[罗纳尔多]希望的那样功能丰富，所以他决定看看自动混合饮料的兔子洞有多深。

首先要做的是安装一个微控制器来处理电机的操作。ATtiny13a 非常适合这项工作，因为它只使用一个输出引脚来控制电机，并且可以配置为在省电模式下仅消耗 0.5 微安。这确保了为微控制器和电机供电的两节 AAA 电池的长寿命。

就操作而言，根据手柄上的按钮被按下的次数，电机以不同的模式运行。它可以持续运行，也可以在预定的时间间隔内运行，只要电源持续，就要确保饮料充分混合。请务必查看以下视频，了解所有操作模式的详细说明。我们当然也可以看到更有趣的饮料的其他可能用途。

 [https://www.youtube.com/embed/ScmhuLAGeVc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ScmhuLAGeVc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


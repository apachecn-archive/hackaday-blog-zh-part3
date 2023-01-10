# 拉皮条我的范围:触摸屏版

> 原文：<https://hackaday.com/2016/02/04/pimp-my-scope-touchscreen-edition/>

你有触摸屏示波器吗？我们也不知道。但是像你在手机屏幕上做的那样左右移动或者扩展任一轴会有多酷呢？[Igor]就这么做了，结果(在广告下方的视频中)看起来棒极了。

我们已经[报道了【Igor】对他的 Siglent scope](http://hackaday.com/2015/10/27/flashed-the-wrong-firmware-swap-out-the-lcd-to-match/) 的上一轮黑客攻击，他通过刷新错误的固件来阻止它，然后通过将屏幕弗兰肯斯坦化到固件想要的盒子中来修复它。但是一旦他染上了 scope-hacking bug，他就不能放弃。

简要概述:Arduino Nano 读取触摸屏，并向示波器发送命令以采取相应行动。[Igor]最初想简单地使用背面的 COM 端口进行控制，但他之前的固件错误更新使这一想法变得没有实际意义。相反，他追求与键盘单元接口的数据总线，逆向工程其协议，并用 AVR 中的自定义代码欺骗按键。

作为这一切的副作用，[Igor]还可以编写一个脚本，从他的计算机上控制范围，他最终将这一切重新放置在你现在看到的漂亮的木制前面板上。它比以前的绝缘胶带外观更上一层楼，新功能非常非常酷。值得称赞。

 [https://www.youtube.com/embed/LIMQLcNBINc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LIMQLcNBINc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


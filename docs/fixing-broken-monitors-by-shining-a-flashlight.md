# 用手电筒修理坏掉的显示器

> 原文：<https://hackaday.com/2016/01/22/fixing-broken-monitors-by-shining-a-flashlight/>

在 EEVblog 上有一个坏了的 LED 电视。这是一台相当标准的 2012 年三星电视，不幸的是，由于湿度过大，柔性电路板上有一点腐蚀。一天，[dyril]打开他的电视，发现大约三分之一的屏幕出现故障。在[dyril]将电视拆开后，发现了一个极其奇怪的修复方法:[用灯光照在腐蚀的柔性电路板上修复了电视](http://www.eevblog.com/forum/repair/why-does-applying-light-onto-a-mylar-ribbon-%27fix%27-my-tv/)。

显然，解决办法是将 USB 灯焊接到电视的电源轨上，然后用热胶水将灯粘在违规电路上。解决问题是一回事，但是理解你为什么解决了问题完全是另一回事。[dyril]不知道为什么这个修复有效，也不知道是否有人能给他一个完整的解释。

电视修好了，虽然你不能对结果提出异议，但有一个迫切的问题:在坏掉的电路板上打一盏灯究竟是如何修好电视的？对 EEVblog 线程的猜测似乎已经决定了类似于树莓 Pi 2 的[光子重置。在 Raspberry Pi 2 中，电源部分使用的小型芯片级封装(CSP)在光照下会出现故障。这重置了圆周率，对于成千上万有圆周率的人来说，这是一个非常有教育意义的关于光子和能量水平的介绍。](http://hackaday.com/2015/02/08/photonic-reset-of-the-raspberry-pi-2/)

EEVblog 给出的最佳猜测是，违规电路板上的芯片处理流向柔性电路的差分信号。这种芯片对光敏感，用光子关闭它可以让另一半差分信号接管。这是一个令人费解的解释，但是这又是一个非常非常奇怪的问题。

您可以查看下面[dyril]的问题和解决方案的视频演示。感谢[Rasz]发送此邮件。

 [https://www.youtube.com/embed/z-3m7UqoIBg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z-3m7UqoIBg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


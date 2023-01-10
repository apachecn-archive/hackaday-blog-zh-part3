# 在酒吧呆了一夜后仍能保持平衡的机器人

> 原文：<https://hackaday.com/2017/09/27/a-robot-that-can-still-keep-its-balance-after-a-night-in-the-pub/>

在我们的伦敦大会之前，最近的一次黑客大会上最吸引人的明星之一是[【Dan】的两轮自平衡机器人](https://trandi.wordpress.com/2017/09/19/self-balancing-robot-v4/)。当形形色色的普通读者群喝了许多上等啤酒，为彼此的作品欢呼雀跃时，它就站在酒吧的桌子上，不顾一切试图颠覆它。

在某种程度上，一个成功的自我平衡器可能看起来令人惊讶地乏味，因为它完成了看似不起眼的任务，只是站在那里，除了四处滚动之外什么也不做，但采取这样一种肤浅的观点掩盖了工程的重大壮举，这给了自我平衡器一个派对把戏。从相当基础的硬件中创造一个并不容易，那么他是怎么做到的呢？

3D 打印的框架容纳一对步进电机来完成这项艰巨的工作，而一块条形板则充当包含 MPU6050 加速度计和 DRV8825 步进电机驱动器的电路板的载体。与此同时，整个节目的大脑开始是一个 Espruino Pico，但后来被转移到一个 ESP32。

有一个包含所有代码的链接 GitHub 库,如果我们在伦敦酒吧看到它的描述对你来说不够好，那么你可以在下面的视频中看到它的运行。

 [https://www.youtube.com/embed/-MJ32Il6_cs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-MJ32Il6_cs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你想尝试制作自己的自动平衡器，你可能也想看看这个简单的设计。如果你在伦敦会议上准备了一个演讲，不要害羞——[把它写在 Hackaday.io 上，并添加到这个列表中](https://hackaday.io/list/27411-uk-unconference-talks)！
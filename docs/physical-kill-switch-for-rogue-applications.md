# 流氓应用程序的物理终止开关

> 原文：<https://hackaday.com/2016/07/09/physical-kill-switch-for-rogue-applications/>

需要是发明之母，但有时挫折也是一个很好的动力。[Maciej]在他的日常工作中用 SPSS 做了一堆统计。 [![silacz](img/b27f5bcd47e5f30d7657776f2bc09f42.png)](https://hackaday.com/wp-content/uploads/2016/06/silacz.jpg) 像大多数复杂的软件一样，它可能会被挂起，而阻止它的唯一方法是手动终止正在运行的进程。显然，这种情况对 Maciej 来说太多了。

他把事情掌握在自己手中，[重新利用一个红色的紧急停止按钮](https://hackaday.io/project/12378-spss-kill-switch)来完成任务。它安装在一个罐子上，内部的微控制器被配置为 USB 键盘。当他按下按钮时，它会打开“运行…”菜单并为他输入`taskkill spssengine.exe`。

我们完全可以看到这种装置的治疗价值。此外，万一 SPSS 吞噬了他的系统内存，一切都接近停顿，微控制器的快速打字手指节省的关键几秒钟可能是一个救命稻草。
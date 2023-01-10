# 彩色发音可能是彩虹连接的关键

> 原文：<https://hackaday.com/2015/12/28/color-sonification-could-be-key-to-rainbow-connection/>

这个假期你有没有看到任何花哨的毛衣？现在有一种方法可以量化他们的活力，同时真正听到他们的声音。康奈尔大学工程系的学生【蒙城齐】和【瑞安兰德】专注于颜色的发音，并将可见光谱转化为可听声音。

他们最初计划使用 OV7670 相机模块的像素样本，但无法从中提取任何有用的颜色数据。无论如何，我们更喜欢他们的 B 计划，那就是使用 CdS 光敏电阻和用于红色、蓝色和绿色摄影的塑料滤色器。落在光敏电阻上的不同强度的光根据电压水平产生不同的图案。实际的声音生成是通过 [FM 声音合成](http://www.soundonsound.com/sos/apr00/articles/synthsecrets.htm)完成的。

不同的 RGB 值之间没有太多的自然声音变化，所以为了让它更有趣，他们创造了不同的乐器，根据颜色以不同的速度和音高播放不同的模式。除了音频反馈，RGB 值还实时显示在一个小 TFT 上。下面是显示每种颜色电压的动态条形图。

休息后看看演示；他们在项目中走一遍，在不同的东西上试一试，听听它们的颜色。

 [https://www.youtube.com/embed/n5L-24PfLXU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n5L-24PfLXU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


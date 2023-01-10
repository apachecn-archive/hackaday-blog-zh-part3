# LED 钟摆脉冲出钟面

> 原文：<https://hackaday.com/2015/10/17/led-pendulum-pulses-out-clock-face/>

你不得不承认[迪伦·拉什]的[钟确实是一个摇摆的](http://blog.dylanhrush.com/2015/08/the-pendulum-clock.html)r。你见过安装了发光二极管的手臂扫出信息的桌面创意吗？[迪伦]做了同样的事情来制作一个时钟，但他没有画数字，而是画了一个模拟钟面。你知道那种有胳膊的圆东西吗？

时钟后面是一个驱动 MAX7219 LED 控制器的 Arduino。使用 MAX7219 是一个挑战，因为它需要一个 led 网格，而时钟需要一个线性阵列。[Dylan]使用了一系列单独的发光二极管来匹配控制器想要的。旋转编码器告诉处理器手臂的位置，因此 Arduino sketch 可以确定应该点亮哪些 led 来显示时间和钟面。

更令人惊奇的是[迪伦]在钟表变得声名狼藉之前就创造了这个。

休息后转到视频。

 [https://www.youtube.com/embed/Z96pdkLdfd4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Z96pdkLdfd4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


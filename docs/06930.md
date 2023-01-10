# 一种用于燃烧人装置的火焰二极管指示灯传感器

> 原文：<https://hackaday.com/2017/08/28/a-flame-diode-pilot-light-sensor-for-a-burning-man-installation/>

明火是电离气体的复杂混合物，具有意想不到的特性。正如你所预料的那样，大量的电离产生了一定程度的导电性，但是不寻常的特性是火焰只能向一个方向传导。换句话说，它可以变成某种二极管，就像真空管二极管一样。

[Paul Stoffregen]已经在一个火焰探测器中利用了这种现象，他建造了这个火焰探测器，安装在一个基于燃烧的人火焰艺术装置上。它是对传统指示灯问题的部分回应:当风吹灭指示灯时，未点燃的气体云会积聚。如果火焰不再存在，传感器允许指示灯自动重新点燃。

电路出奇的简单，PNP 晶体管由置于基极电路中的火焰二极管开启。这允许测量火焰的强度以及它是否存在，并且全部以微小的电流消耗为代价。一个电容器由晶体管充电，充电时间由一个计时器测量，用来估计火焰强度并在必要时触发指示灯。有趣的是，它来自于一项 2013 年到期的专利，在你的调查中包含这一特定的研究领域总是值得的。

所有的构造细节都在上面链接的页面中，你可以在 break 下面的视频中看到测试中的系统。

 [https://www.youtube.com/embed/8rv_m6Fr8Lg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8rv_m6Fr8Lg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前已经研究过火焰的这种特性，在一个项目中，有人制作了一个正常工作的火焰三极管。
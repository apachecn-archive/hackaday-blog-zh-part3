# 直升机的钟摆很漂亮

> 原文：<https://hackaday.com/2016/11/08/helicopter-pendulum-is-pid-licious/>

如果你曾经试图调整一个 PID 系统，你可能会遇到相等部分压倒数学和黑魔法民间智慧。或者，您可能只是让自动调优接管。如果你真的想对运动控制算法，包括 PID 算法，有一些好的直觉，没有什么比动手实验更好的了。

为了让你入门，[克洛维斯]写了他的[预算基于螺旋桨的 PID 演示平台](http://fritzenlab.com.br/2016/11/sistema-pendulo-helice-experimentos-fisicos/)(葡萄牙语，翻译得非常好[这里](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=http://fritzenlab.com.br/2016/11/sistema-pendulo-helice-experimentos-fisicos/&edit-text=&act=url))。

基本设置是一个粘在烤肉叉上的电位计，末端有一个迷你四轴飞行器电机和转子。微控制器读取电压，并通过 MOSFET 对螺旋桨进行脉宽调制。目标是让钟摆稳定地悬停在半空中，由你在控制器上能想到的任何算法来控制。[Clovis]'视频演示了风扇的开关和 PID 控制。增加几个电位计(一个用于 P、I 和 D？)会让动手调整变得更加互动。

总的来说，这个系统只会让你花费几美元，但能教会你的东西比你在大学一个月学到的还多。很有可能你手头上没有和他一样的沙丁鱼罐头，但这里需要一些即兴创作。

如果你不知道为什么你想掌握~~开环~~闭环控制算法，这里有一个我们很久以来见过的最好的[广告之一。但你不必一开始就用手动上弦的百元电机，或者精密加工的钻头。正如[克洛维斯]所展示的，你可以用一架坏了的四轴飞行器和你在厨房里找到的任何东西来凑合。](http://hackaday.com/2016/09/14/furuta-style-inverted-pendulum-is-king-of-geek-desk-ornaments/)

 [https://www.youtube.com/embed/jOZmHBkXkCM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jOZmHBkXkCM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


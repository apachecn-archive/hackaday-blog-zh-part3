# 用该死的激光束(指着它们的大脑)寻找老鼠，建造一个激光控制器

> 原文：<https://hackaday.com/2016/08/13/the-quest-for-mice-with-frickin-laser-beams-pointed-at-their-brains-building-a-laser-controller/>

[![The logo for the field is kind of cute though.](img/dfd74d9f20ddf8ac72f1ed059554b43c.png)](https://hackaday.com/wp-content/uploads/2016/07/fl201501161528355315.jpg)

The logo for the field is kind of cute though.

[斯科特·哈登] [正在从事一项涉及光遗传学](http://www.swharden.com/wp/2016-07-28-opto-isolated-laser-controller-build/)的研究项目。从我们所能拼凑出来的来看，光遗传学是这样的:有人从基因上改造了一只老鼠，使其具有能被光敏蛋白激活的细胞行为。这些老鼠的头上安装了一个该死的激光器，但指向它们的大脑内部，而不是指向邦德先生的大脑。

自然，要猜测鼠标的输出行为，输入光必须非常精确和可控。[斯科特]有一个激光器和一个驱动器，但他没有一个控制器来发射脉冲。让事情变得更困难的是，研究已经在进行中，而且必须制造控制器

昂贵的激光驱动器有一个奇怪的输出，可能是正 28 伏，也可能是负 28 伏……8 安培。这是一个非常小的行业的行业标准。他没有真正好的方法来测量或验证这一点，而不破坏他的测量设备或激光驱动器。因此，他决定在控制器上构建一个电压无关的输入。另外，光隔离输入可以保护昂贵的控制器。

[![The kind of travesty that can occur when [Stefan Kiese] doesn't have access to nice project boxes. ](img/3dfb717173f1d9eceda73997d055b0c1.png)](https://hackaday.com/wp-content/uploads/2016/07/img_3466.jpg)

[当【斯科特】无法访问漂亮的项目框时，可能会发生这种滑稽的事情](http://www.swharden.com/wp/2010-06-03-aj4vd-qrss-vd-mept/)。

输出由 ATtiny85 处理。他承认，555 电路可以产生他需要的信号，但要获得精确的脉冲，更容易的是将微控制器连接到晶体上，并知道它是 100%正确的。否则他将不得不整天用示波器摆弄电位计。只有少数 Hackaday 的读者将这种想法视为放松的周日下午。

他把所有东西都打包在一个漂亮的项目箱里。他把它们放在手边，以防止他在能找到的任何东西上建立电路。从业余无线电爱好中加入一些技巧，使盒子看起来非常专业。他很高兴也很惊讶地发现这个盒子在他的第一次尝试中就成功了。
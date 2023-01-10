# 矢量网络分析仪采用 SoC FPGA

> 原文：<https://hackaday.com/2018/05/09/vector-network-analyzer-uses-soc-fpga/>

如果你正在使用交流电路，矢量网络分析仪(VNA)是非常方便的。作为学生 InnovateFPGA 竞赛的参赛作品，[Evgenii Vostrikov]、[Danila Nikiforovskii]和[Daniil Smirnov][使用一个 DE10-Nano 高速模数和数模转换器以及一个循环器创建了一个 VNA](http://www.innovatefpga.com/cgi-bin/innovate/teams.pl?Id=EM078)。大多数细节都在下面的视频中，以及该项目的 [GitHub](https://github.com/tvShushtov/em078_vector_analyzer) 页面上。

DE10-Nano 在一个封装中集成了双核 ARM 处理器和 Altera FPGA。这样，您就可以在有意义的地方使用 CPU，同时在需要高性能的地方利用 FPGA。

循环器使用运算放大器将测试信号路由至被测器件，同时将任何反射信号导回器件进行测量。该设计还使用了[锁定放大器](https://hackaday.com/2017/09/27/lock-in-amplifiers/)，这是我们最近讨论过几次的东西。这使得成本较低的转换器能够产生幅度和相位信息。

根据视频中的风扇判断，我们怀疑设置有点热。GitHub 页面上有很多俄语，所以我们不确定我们能猜出多少，因为我们的俄语技能主要来自观看驼鹿和松鼠的冒险。

如果你对 VNA 感兴趣，它们不再像以前那么贵了。特别是，如果你[推出自己的](https://hackaday.com/2016/08/13/a-vna-on-a-200-euro-budget/)，并且已经在你的垃圾箱里有一些东西。

 [https://www.youtube.com/embed/BvW69keXv7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BvW69keXv7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


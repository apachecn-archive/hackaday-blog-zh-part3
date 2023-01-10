# 台式电源使用服务器电压调节器

> 原文：<https://hackaday.com/2017/01/24/bench-power-supply-uses-server-voltage-regulator/>

如果你把一台电脑和一堆其他机器塞进一个机架里，你最好把它做成一台结实的机器。服务器级意味着一些东西，因此在项目中使用服务器部件，如使用服务器电压调节器的高功率电源，可以将它带到更高的鲁棒性水平。

但是在[安迪·布朗]建造这种电源之前，他必须对模块进行逆向工程。根据他所了解的情况，以及模块的数据手册，他设计了一个控制器来利用它们的所有功能，最终得到了一个全功能电源。这些模块在 3.3 伏电压下的额定总功耗为 66 瓦，并有一个次级 5 伏输出。使用 ATmega328，[Andy]能够控制模块，显示电压和电流、温度检测和风扇控制，甚至可以通过 UART 将数据记录到串行端口。他的设计主要以通孔组件为特色，让每个人都可以使用。一个合适的案例还没有出现，我们期待着看到成品。

不能在易贝上拼凑一些这样的模块？或者比起开关模式，你更喜欢线性电源？别担心——这里有[一个超级稳定的无调节电源给你](http://hackaday.com/2016/10/29/build-the-simplest-bipolar-power-supply/)。

 [https://www.youtube.com/embed/nAsno43i6HU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nAsno43i6HU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Orkhan]的提示。
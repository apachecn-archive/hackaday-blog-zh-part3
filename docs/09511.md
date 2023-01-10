# Alexa 和 Particle 让咖啡机变得更加现代化

> 原文：<https://hackaday.com/2018/05/21/alexa-and-particle-modernize-coffee-machine-by-one-iota/>

当[史蒂夫·帕克]的女朋友得到一个可以接受语音命令的茶壶时，他突然把他的花式咖啡机视为一个技术恐龙。它可能可以煮出很好的咖啡，但让德隆基运转起来很不方便，因为它每次打开或关闭时都会运行一个自我清洁周期。

[于是开始了[史蒂夫]试图通过粒子光子](https://stevep.xyz/2018/05/17/delonghi-magnifica-now-with-alexa/)打开 Alexa 的冒险。由于机器的设计方式，简单地增加一个继电器是不行的——机器只会关闭再打开，然后再次开始自清洁。一旦进入，他发现它是由 PIC18LF2520 控制的。进一步的研究表明，它由一个离线开关供电，该开关将功率 MOSFET 与电源控制器相结合。[Steve]发现按钮是通过方波读取的，并由多路复用器解释。

当(史蒂夫)试图用山寨版 Saleae 解读信号时，这个项目陷入了困境。他一插上电源，控制板就烧了，因为德隆基显然没有参考地球。在等待替换电路板到达时，他尝试更换 mux 和移位寄存器芯片，这实际上修复了电路板。然后或多或少的是使用德隆基的状态 led 来确定机器的状态，然后与光子和 Alexa 接口。循环通过休息时间进行一次里斯特雷托大小的演示。

[史蒂夫]做这些并不是为了真正制作咖啡，只是用语音命令打开机器。不过，光子完全有能力制作咖啡，正如我们在[看到的这款闭环咖啡机](https://hackaday.com/2017/12/13/will-hack-for-espresso/)。

 [https://www.youtube.com/embed/QRecgo4liN4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QRecgo4liN4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 复古 IBM Daisywheel 打印后再次逆向工程

> 原文：<https://hackaday.com/2017/01/14/vintage-ibm-daisywheel-prints-again-after-reverse-engineering/>

就在个人电脑时代来临之前，IBM 打字机凭借 Wheelwriter 系列达到了技术顶峰。这是一台雏菊轮打印机，具有可互换的打印头、记忆功能和初步的文字处理能力，在被个人电脑超越之前，轮子打印机从未有太多的时间发光。Wheelwriter 现在非常便宜，并且像许多 IBM 产品一样非常容易被黑客攻击，正如[所示，这个简单的 Arduino 接口将 wheel writer 变成了打印机](https://www.youtube.com/watch?v=Awxbu8y5cv8)。

[Chris Gregg]喜欢玩打字机——他甚至弄了一台旧的 Smith Corona 来演奏[勒卢瓦·安德森]的*The Typewriter*T3——他对这些大部分过时但可爱的机电文物非常在行。将个人电脑与 Wheelwriter 连接起来可能就像为机器找一个原始接口卡一样简单，但那些就像母鸡的牙齿一样，此外，这还有什么意思呢？所以[Chris]将一个逻辑分析仪连接到一个标记良好的端口上，这个端口本应连接到接口卡上，通过敲击键盘对这个有点奇怪的串行协议进行逆向工程。他为 Wheelwriter 设计的接口非常简单——只是一个浅蓝色 Bean Plus 和一个 MOSFET，用于在正确的时间内驱动总线高低电平。其结果是相当于字母数字打印机，但用一点额外的代码一些点阵图形也是可能的。

在花了大量时间对串行通信进行逆向工程后，我们可以体会到这需要完成的工作量。想做类似的事情，但没有钱买逻辑分析仪？也许[你可以腾出 22](http://hackaday.com/2016/12/13/compiling-a-22-analyzer/) 美元，开始破解一个类似的令人印象深刻的黑客。

 [https://www.youtube.com/embed/Awxbu8y5cv8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Awxbu8y5cv8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [r/arduino](https://www.reddit.com/r/arduino/comments/5mi7qb/my_1980s_ibm_typewriterteletype_hack/)
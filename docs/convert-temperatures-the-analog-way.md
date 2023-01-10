# 以模拟方式转换温度

> 原文：<https://hackaday.com/2017/08/10/convert-temperatures-the-analog-way/>

大家都知道怎么把摄氏温度换算成华氏温度吧？在数字温度计上，你只需轻触小开关，在天气应用程序上，你可以改变设置，或者如果情况变得更糟，你可以让谷歌为你计算。但是如果你想用老办法解决问题呢？然后你拿出几个运算放大器，[进行模拟式转换](http://www.kerrywong.com/2017/08/06/converting-celsius-to-fahrenheit-the-analog-way/)。

我们之前已经了解过[简单的运算放大器电路如何进行基本的数学运算](http://hackaday.com/2016/06/19/make-math-real-with-this-analog-multiplier-primer/)，而【Kerry Wong】想要求解的方程甚至更简单。回想老 T*[f]*= 9/5t*[c]*+32 的公式(且抛开公制与传统单位的优劣；我们已经听够了[中的论点](http://hackaday.com/2017/01/13/whats-so-bad-about-the-imperial-system-anyway/))，【Kerry】带我们看了一个简单的双通道运算放大器电路，将热电偶模块的 1mV/°C 输出转换为 1 mV/ F。调整由一个同相放大器负责，其电阻选择为提供 1.8 的增益，而失调则由一个差分放大器处理，该放大器向调整后的输入增加 32 mV。策略性放置的调整器允许[凯瑞]调整电路以给出正确的转换。

对于这样的工作，很容易在 Arduino 上使用模拟输入，并在代码中处理转换。但是很高兴知道如何用老方法做这件事，并向[Kerry]致敬，他向我们展示了细节。

 [https://www.youtube.com/embed/jYeWkp4v3nE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jYeWkp4v3nE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


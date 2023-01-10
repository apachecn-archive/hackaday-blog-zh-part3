# AMSAT MPPT 走向无限和超越

> 原文：<https://hackaday.com/2017/11/27/amsat-mppt-goes-to-infinity-and-beyond/>

业余无线电卫星公司 AMSAT 与罗彻斯特理工学院的学生联手，创造了一个与福克斯-1B 立方体卫星相连的 [MPPT。11 月 18 日，它被绑在 Delta II 火箭的后面，成功发射进入轨道。这种模拟 MPPT 或最大功率点跟踪器用于根据 10 厘米 x 10cm 厘米卫星上太阳能电池板的输出优化电池的功率。简而言之，这是通过匹配两者的电压来实现的。如果你还没有机会亲自体验一下，Hackaday 的[埃利奥特·威廉姆斯]写了一篇关于辉煌的 MPPT 效率](https://faradayrf.com/ham-radio-is-about-more-than-radios-amsat/)的[详尽解释。](https://hackaday.com/2017/03/17/are-you-down-with-mppt-yeah-you-know-me/)

这个小家伙目前每 90 分钟在轨道上飞驰一次。在每一个椭圆轨道上，卫星都会经历剧烈的加热和冷却循环。该小组计算出，在为期 5 年的任务中，这个包裹将总共绕地球运行 29，200 次。这意味着有 29，200 次测试可以让它在压力下破裂——真的。更困难的是，本科生团队没有资金进行自动化电路板组装。这意味着他们必须将超过 400 个微型元件手工焊接到电路板上，增加了额外的人为错误，从而增加了故障的可能性。但到目前为止，这只小狗很强壮。这真实地展示了通过一点努力、艰苦的工作和普通的良好工程就能克服的困难。

他们为这个项目制作了一些看起来很犀利的文档。我强烈建议花几分钟时间阅读他们的 [Fox-1 MPPT 文档](https://github.com/FaradayRF/Fox-1-MPPT/blob/master/Documents/Fox-1_MaximumPowerPointTracker.pdf)，如果你有兴趣看到仔细思考过的设计细节。上面显示的原理图用于预测最大功率点电压。模拟计算机使用 Y = mX + B 来精确预测基于太阳能电池板温度的 MPPT。通过这样做，他们能够解释在轨道上导致比特翻转的辐射。理解所有这些因素对这只小动物的成功至关重要。

我们想对 Bryce Salmi、Brenton Salmi、Ian MacKenzi 和 Daniel Corriero 的 RIT 团队在未来的努力中祝他们好运。将任何东西送入太空，然后在到达后保持运行不是一件容易的事情，已经有另一个 MPPT 将于 2017 年 12 月在维珍银河发射装置一号上用 Fox-1E CubeSat 发射。看看下面他们做的一些必要的测试，以确保这将是一次成功的任务。如果你和我们一样认为这是一次了不起的合作，请告诉我们。

 [https://www.youtube.com/embed/TN7gRVWHZM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TN7gRVWHZM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


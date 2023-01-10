# 本周失败:瓦特失败

> 原文：<https://hackaday.com/2016/01/21/fail-of-the-week-watt-a-loss/>

这一个有点过时了，但是教训仍然是相关的。[Zach Hoeken]发布了他在构建 CNC 步进驱动器时面临的挑战。早在 2012 年，他就在用东芝电机驱动器做实验。

他构建的模块化电机驱动板基于 THB 6064 ah——能够实现 1/64 步，最高 50V 时为 4.5 安培。[扎克]建立了一个测试夹具来运行板通过他们的步伐。几个乱七八糟的轨道是他的问题中最小的——通过切断轨道和使用跳线纠正错误，很容易修复。但是电机驱动板的接头尺寸颠倒了。唯一的解决办法是在背面焊接接头。

```
LESSON : Always check footprint orientation and pin numbering before sending boards to fab.
```

令人惊讶的是，像扎克这样有经验的人搞砸了欧姆定律。根据他希望电机运行的电流，他的检测电阻需要为 3.2W，但他使用了 SMD 封装(可能为 0805)。那些微小的电阻根本不能用，5W 的电阻看起来像一个丑陋的黑客。

```
LESSON : *Remember the basics. High current tracks, power components, high speed digital layout, shielding, heat sinking and the many other parameters to keep in mind while designing boards*.
```

最后，零件号混淆被证明是他最大的挑战。THB6064AH 与 THB6064H 不同。差别不是很多，但足以让他怀疑芯片本身以外的一切。好的一面是在探索和测试的过程中学习了大量的东西，从而找到了问题的根源。

```
LESSON : *Please make sure your BoM lists exact part numbers used in your designs*.
```

一个例子是将 ATmega328P 和 ATmega328 混淆——芯片具有不同的签名、掉电和功耗。很容易修复，但这可能会导致一些紧张的时刻，而试图找出它。

如果你想知道以前在哪里听过这个名字[扎克·霍肯]，他是 Makerbot 的创始人之一。

感谢[Peter Montgomery]，他在搜索东芝步进驱动芯片时偶然发现了这个提示。

* * *

《一周失败》是一个黑客专栏，它把庆祝失败作为一种学习工具。通过写下你自己的失败和[给我们发送一个故事的链接](mailto:tips@hackaday.com?Subject=[Fail of the Week])——或者发送你在互联网旅行中发现的失败报道的链接，帮助保持乐趣。
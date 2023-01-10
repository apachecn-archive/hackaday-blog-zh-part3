# 设计分析:核心 XY Vs H-Bot

> 原文：<https://hackaday.com/2016/02/29/design-analysis-core-xy-vs-h-bot/>

黑客作家[约书亚·瓦斯奎兹]在他的个人网站上写了 3D 打印机常用的 [Core-XY 和 H-Bot](http://www.doublejumpelectric.com/projects/core_xy/2014-07-15-core_xy/) 运动之间的机械差异。一个初学机械设计的人在着手制作一个机芯时，可能会忽略很多事情。有时候，在这些运动的情况下，它们不是很明显，就像在代码中找到一个麻烦的[模式](http://hackaday.com/2015/11/13/code-craft-embedding-c-timing-virtual-functions/)；在未来的设计中，在人们意识到它们之前，必须展示出来。

[Joshua]首先描述每个动作是如何工作的。乍一看，H-Bot 运动似乎比 Core-XY 更简单有效。Core-XY 使用更多的皮带，并且一些滑轮彼此不在一个平面内。然而，这样做是为了消除 H-Bot 设计中施加在框架上的力矩。这一瞬间可能会以不可预测的方式破坏机芯的准确性。

核心 XY 运动是我们最喜欢的运动之一。它使马达保持静止。它紧凑、精确、可重复、线性。很好的理解了这其中的机械原因。就像学习 SQL 数据库调用一样，一个库会让你写更好的代码。
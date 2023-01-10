# 一个锂离子增压包，做对了

> 原文：<https://hackaday.com/2018/05/27/a-li-ion-booster-pack-done-right/>

我们都习惯了包含锂离子或锂聚电池和一点逆变电路的电池升压包，当智能手机电池寿命不如广告所示时，它们是 21 世纪日常生活的标准组成部分。但是，我们中有多少人考虑过它们包含了什么，又有多少人试图生产出尽可能好的产品，而不是以最低价格建造的产品呢？

这是[Peter6960]遵循的路线，生产了位于 18650 电池座背面的 PCB。它遵循[【great Scott】](https://www.youtube.com/watch?v=Fj0XuYiE7HU)的工作，特别是在使用 TP4056 充电器、MT3608 升压转换器和 FS312F 保护 IC 方面。许多商用模块省略了任何保护电路，而 FS312F 尤其令人感兴趣，因为它具有 2.9V 的低截止电压，可以延长电池的寿命。PCB [的文件可以在 Google Drive](https://drive.google.com/file/d/1W-qs7dp2oDAhGEn1Lan2roVbdYYN5YTz/view) 上的 zip 文件中找到。

你可能认为关于锂离子电池升压器没有什么新的东西可以学习，但它总是值得一看一个执行良好的作品。我们注意到他指的是 Li-poly 电池，而使用的似乎是锂离子 18650 电池。很可能这只是一个疏忽。

关于锂化学可充电电池的特性和安全性有很多需要了解的，你可能会发现[【肖恩·博伊斯】关于这个主题的文章](https://hackaday.com/2017/09/18/the-science-behind-lithium-cell-characteristics-and-safety/)是一篇有趣的读物。
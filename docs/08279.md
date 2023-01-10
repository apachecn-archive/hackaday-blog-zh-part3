# 复古翻转时钟得到翻新

> 原文：<https://hackaday.com/2018/01/23/flip-clock-retrofit/>

复古技术几乎总是适合黑客攻击——无论是怀旧，教育拆卸，还是承认和保护我们站在上面的肩膀。偶然发现一个旧的西德制造的翻转时钟，YouTuber [Aaron Christophel] [改装了这个设备](https://www.youtube.com/watch?v=tvFF8EHjL3Q)，同时保留了它原来的机械部件！

没有某种 led 的现代电子产品是不完整的，所以他在钟面的底部放了一条带子，以增加可见度和凉爽系数。他没有事先告诉时钟的状态，但他能够让时钟的移动部分为它的第二次生命而工作。

控制时钟的是 Arduino Mini Pro 和时钟内部的一个简单的 DS1307 RTC 板。最初，它有一个显眼的外部盒子，里面装有电子设备和电源，现在已经过时了，或者准备改天再用！Arduino 的代码是使用一对库的有效的几行代码。它需要做的只是每分钟翻转电磁电机的极性来更新时间。

我们偶尔喜欢优雅的黑客攻击，有时复古技术[恰好适合那种](https://hackaday.com/2014/12/13/simple-and-elegant-single-digit-nixie-tube-clock/)。
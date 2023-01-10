# Valhalla 可编程精密标准的修复与校准

> 原文：<https://hackaday.com/2016/01/25/repair-and-calibration-of-valhalla-programmable-precision-standard/>

精密标准是测试和测量仪器的顶峰。当然，设计得很好，但也建造得很漂亮，无论它们有多古老，都是一场盛宴。[Shahriar]在“信号路径”经常给我们这样的设备瘦。在最新一集里，我们看到了一个 [Valhalla 2701C 可编程精密 DC 电压标准](http://thesignalpath.com/blogs/2016/01/19/teardown-repair-calibration-of-a-valhalla-2701c-programmable-precision-dc-voltage-standard/)。

即使按照 1990 年的标准，这也是一种相当基础的仪器，只能产生 100 毫伏到 1200 伏的 DC 电压。但它是一个参考标准，所以输出高度稳定，准确和精密。他从易贝廉价购得，但运输似乎造成了一些损害。当他按下按钮时，它会打开，继电器会发出滴答声，但 7 段 LED 显示屏是空白的。幸运的是，打开顶盖可以解决这个问题——只是前显示屏和主板之间的连接松动了。检查还表明，增加 120 毫安 DC 电流范围需要在主板上增加额外的组件，因此他快速升级固件的希望是短暂的。

[Shahriar]借此机会带我们参观了建造良好的单元的各个部分。很明显，在它的一生中，它经历了一些修复。一些电容器看起来有变化，继电器外壳被烙铁损坏。数字部分主要是 6800 微控制器、EPROM 和 NVRAM，它产生产生输出电压所需的 PWM 信号。高精度参考信号对于这种设备至关重要，这款设备使用带有“定制”后缀的 [LM299](http://www.ti.com/lit/ds/symlink/lm399.pdf) ，这意味着它经过特殊筛选和装箱。他做了一个快速的校准运行，但显然是仓促的，没有产生稳定的结果。但这也可能是由于他使用的低质量电缆，或其他一些因素。校准这样的设备是一项既需要时间又需要耐心的工作。

虽然这可能不会让你大吃一惊。为此，看看这篇文章，在这篇文章中[Shahriar]拆除了价值 100 万美元的 Labmaster 10-100zi 示波器，或者在另一篇文章中，他摆弄着[一台价值 50 万美元的示波器，你可能永远不会使用，更不用说拥有](http://hackaday.com/2013/08/14/playing-with-an-oscilloscope-youll-probably-never-own/)。

 [https://www.youtube.com/embed/e-UwxRhYLS8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e-UwxRhYLS8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [危险原型](http://dangerousprototypes.com/2016/01/21/teardown-repair-calibration-of-a-valhalla-2701c-programmable-precision-dc-voltage-standard/)
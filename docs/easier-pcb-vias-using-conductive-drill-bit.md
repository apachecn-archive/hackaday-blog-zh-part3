# 利用钻孔技巧和导电油墨简化 PCB 过孔

> 原文：<https://hackaday.com/2015/11/23/easier-pcb-vias-using-conductive-drill-bit/>

如果你曾经在没有专业设备的情况下制作过双面印刷电路板，你必须处理好将电路板的一面连接到另一面的问题。你有几个显而易见的选择:1)依靠元件引线连接两侧(并焊接两侧)；2)在电路板的两侧创建过孔和焊线；或者 3)使用通孔铆钉。[Diyouware]有一个不同的想法:使用导电墨水。在几次失败的尝试后，他们发现了一种似乎很有效的技术。

这不是我们第一次听说有人尝试导电墨水并取得不同程度的成功。通常，最大的问题是墨水想从孔中流出。[Diyouware]对这个问题有一个有趣的解决方案:不要把洞钻透。

为了可靠地做到这一点，[Diyouware]改装了一台钻床，以便在钻头接触底层铜时获得信号。结果是形成阱的盲孔。稍后用导电墨水填充该阱是一件简单的事情。虽然你可以手工填充通孔，但[Diyouware]使用了一个自动点胶机，并用 Eagle 用户程序的输出来控制它，将通孔图案转换成机器指令。你可以在下面的视频中看到实验板的创建。

值得注意的是，当你有一个专业制作的 PCB 时，他们通常会在空白板上钻孔，然后进行电镀，因此引脚和过孔可以毫无困难地导通。除了电镀之外，这也使得艺术品与孔精确对齐变得很困难。还有[其他专业工序](http://hackaday.com/2015/03/31/meet-the-machines-that-build-complex-pcbs/)，钻孔后电镀板材，电镀部分[可以](https://www.youtube.com/watch?v=fY0AjzKLA-8)。

LPKF 有一种伪造电镀通孔的方法，也是[使用导电胶](http://www.lpkf.com/products/rapid-pcb-prototyping/through-hole-plating/chemical-free/index.htm)。当然，获得良好电镀通孔(和洞)的一个简单方法是[继续专业制作电路板](http://hackaday.com/2015/09/21/why-are-you-still-making-pcbs/)。

 [https://www.youtube.com/embed/oJyoXwNONho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oJyoXwNONho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 3D 印刷电路板…算是吧

> 原文：<https://hackaday.com/2016/12/17/3d-printed-circuit-boards-sort-of/>

喜剧演员迪米特利·马丁对“有点”这个短语做了一点解释。他说:

> “说‘有点儿’是一件无害的事情……有点儿。它只是一个填充物。算是吧……其实没啥意思。但在某些事情之后，就意味着一切。就像…在“我爱你”之后…或者“你会活下去的。”

SCADboard 是一个 OpenSCAD 库，可以让你创建 3D 可打印电路板…算是吧。图书馆的布局就像一块试验板，两边各有两根母线，由行和列组成一个网格。OpenSCAD 模块提供了一种创建电路板、集成电路、发光二极管、电线和其他基本组件的方法。您设置了一些初始变量(如板厚)，然后您的代码如下所示:

```
 wire(1,bln,1,e, neg); // Neg left trace to LED
 led(1,e+1, 1,e+2, yellowled); // LED
 wire(1,f, 1,i, pos); // LED Pos
 wire(1,j, 1,brp, resistor); // Resistor

 wire(3,c,3,h, pos); // Cap Pos
 wire(4,c,4,h, neg); // LED Resistor

```

有什么问题吗？可以打印出来，但是没有导电性。有一些小槽供你放置电线。作者建议你把电线拧在一起。你可以焊接它们，但如果这样做，你必须小心不要让塑料板热到融化。这可能需要一些技巧或散热。这当然需要稳定的手和快速焊接。我们想过用 Kapton 胶带覆盖印刷基板，并在上面打孔，让电线穿过孔，但我们不确定这在实践中会有多好。

不过，很明显，它确实有效。他们设计了一个简单的 Arduino 板作为概念验证。这是一个电路板……算是吧。[Brian]一直在做他的系列关于[在所有东西中制作 PCB](http://hackaday.com/2016/09/22/making-a-pcb-eagle-part-1/)，但我们怀疑这是否符合要求。话又说回来，你真的再也不需要[制造它们了。](http://hackaday.com/2015/09/21/why-are-you-still-making-pcbs/)
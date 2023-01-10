# Hackaday 奖参赛作品:DIY ARM 科学计算器

> 原文：<https://hackaday.com/2017/04/20/hackaday-prize-entry-diy-arm-scientific-calculator/>

当黑客想要某样东西却买不起时，他或她会怎么做？当然，他们一起破解了一个。或者，在[拉蒙·卡尔沃]的案例中，他们深思熟虑地计划和原型。[拉蒙·卡尔沃]想要一个科学计算器，但是他买不起，所以他自己设计并制造了一个。

[Ramón]从 Arduino 开始，但最初升级到飞思卡尔的 Freedom KL25Z 开发板，升级到使用 mbed 编程的 ARM Cortex-M0+。显示器是一个电子组件 DOGL-128 128×64 像素液晶显示器。[Ramón]在 PCB 上做了几次迭代，从一个大的 DIY 版本以便 Arduino 版本工作，到当前的较小版本，用于带有手工焊接 SMD 元件的 ARM 芯片。之后，[Ramón]研究了解析数学输入所需的算法。他选定了调车场算法，该算法将输入转换成反向波兰符号(RPN ),这样软件更容易使用。

[Ramón]具有大量的功能，包括标准的加、减、乘、除运算、平方根、n 次方根和幂运算、三角学、对数和对数 10 以及阶乘(！)待办事项列表上还有一些事情，比如低功耗和图形模式，系统中还有一些 bug，但整个系统已经启动并运行。[Ramón]已经将原理图和 KiCAD 文件与材料清单一起放在他的 Hackaday.io 项目页面上。

我们有一些以计算器形式出现的 Hackaday 奖参赛作品，比如这个带有[谢妮电子管](https://hackaday.com/2016/05/09/hackaday-prize-entry-a-programmable-calculator-with-nixie-tubes/)和这个模仿 [70 年代惠普计算器](https://hackaday.com/2015/08/18/hackaday-prize-entry-the-70s-called-they-want-this-calculator/)的作品。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)
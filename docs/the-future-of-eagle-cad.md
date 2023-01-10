# Eagle CAD 的未来

> 原文：<https://hackaday.com/2016/07/05/the-future-of-eagle-cad/>

上周，Autodesk [宣布购买 CadSoft Eagle](http://hackaday.com/2016/06/29/the-eagle-has-landed-at-autodesk/) ，这是最流行的电子设计自动化和 PCB 布局软件包之一。

Eagle 已经存在了近三十年，已经发展成为电子爱好者、学生和工程公司的标准 PCB 设计包，其领导者是一位通过 Eagle 学习 PCB 设计的人。这样做的原因很简单:对于大多数简单的设计来说已经足够好了，而且还有一个*免费的*版本 Eagle。唯一可比的开源替代品是 KiCad，它没有 Eagle 那么多的忠实追随者。无论好坏，Eagle 是一个标准，从 [Sparkfun](http://www.opencircuits.com/SFE_Footprint_Library_Eagle) 到 [Adafruit](https://github.com/adafruit/Adafruit-Eagle-Library) 的开源公司都虔诚地使用它，并创建了高质量的部件库和多个教程

我有机会与[马特·博格伦]交谈，他是前黑客霸主，现任 Autodesk Circuits 总监。他是欧特克所有电子设计产品的最终负责人，从 [Tinkercad](https://www.tinkercad.com/) 、 [123D](http://www.123dapp.com/) 、 [Ecad.io](https://www.ecad.io/) ，到 project Wire，这是欧特克 3D 打印机 [Voxel8](http://www.voxel8.co/) 背后的引擎，也可以打印电子产品。[Matt]现在是 Eagle 的主人，最终将决定什么会改变，什么会保持不变，以及 Eagle 的发展道路。

### Eagle 许可证

Eagle 因其软件的免费版本而闻名。20 年前，在 Protel 和其他昂贵的 EDA 和电子设计包的时代，Eagle 一直有一个有限的免费软件版本。可以说，这就是 Eagle 受欢迎的原因；免费教育版本意味着学校可以使用它，这些学生将带着使用他们已经知道的知识的愿望进入劳动力市场。Eagle 的免费版本意味着电子爱好者可以在家里使用专业人员使用的相同工具设计自己的 PCB。免费软件版本不会消失。

除了免费软件版本，为 Eagle 购买正确的许可证并不容易。上周， [Eagle 有五个版本可用](http://www.cadsoftusa.com/eagle-pricing/)，有不同的插件组合，如原理图、布局和自动布线器。每个版本都对原理图、信号层和布线区域的数量有限制。对于单用户许可证，有将近 50 种不同的选项，价格各不相同。

现在只有 6 只鹰的产品。商业许可证的范围从一个原理图、两个信号层和一个 100x80mm 的布线区域到具有 16 个信号和一个 4 平方米布线区域的最终许可证。对于非商业许可，免费教育版包含 99 个原理图、6 个信号层和一个 160x100mm 毫米的布线区域。这是鹰与时俱进；一名新工程师必须知道如何在电路板上铺设天线、阻抗控制馈线、DDR 路由、如何断开大型 BGA 以及多层板能够实现的一切。

谈到 Autodesk 许可，一个大问题是地平线上隐约出现的祥云。互联网是一个东西，现在软件电话回家。 [Altium 的电路制造商被无情地捆绑在这个云](http://hackaday.com/2015/06/20/altium-gives-away-the-farm-with-new-circuit-maker-software/)上，将你的设计锁在一个在线金库里。Autodesk 的 Eagle 也会这样吗？

当然，Eagle 将与其他 Autodesk 产品集成在一起——Autodesk 收购 Eagle 的全部目的是进行全栈硬件开发，从机械设计到电子设计。这是否意味着 Eagle 将成为一个只订阅的模型仍然悬而未决，但从不经意的观察者的立场来看，这是值得怀疑的；仍然有 Eagle 的永久许可，现在这就是 Autodesk 正在出售的。

[![FB](img/5323cde06c6daeb642703ab09c9856b7.png)](https://hackaday.com/wp-content/uploads/2016/06/fb.png)

The most common (and dreaded) error in EAGLE

### 新功能

尽管在 PCB 设计方面它是一个近乎标准的产品，但它还有很多 Eagle 没有的特性。要对一个项目进行设计或电气规则检查，你必须按一个按钮——这不会自动发生。将会有一个长时间的，艰难的观察刚果民主共和国和 ERC。欧特克也“肯定会密切关注路由。”无论这意味着推和推路由，拖动轨迹，还是其他任何东西，KiCad 的最新版本[做得非常好](https://www.youtube.com/watch?v=CCG4daPvuVI)是悬而未决的，但必须注意的是，Eagle 现在是 Autodesk 的首要 EDA 套件。

[马特]计划对媒体说些什么？Eagle 的核心，主要是层次结构、模块化、机械集成(与其他 Autodesk 产品的集成保持一致)和修订管理。这是否意味着可怕的 *F/B 注释已经被切断！*通知是否会最终消失仍悬而未决，但人们只能抱有希望。

随着新方向的到来，UI 可能会发生变化。十五年前，在一台机器上安装 Autocad 会很快磨掉你的退出键上的字母。更现代的 CAD 软件包，如 Autodesk Fusion 和 Inventor 要简单得多。即使是最复杂的软件，界面也变得越来越简单，Eagle 的巴洛克式用户界面没有理由不进行一些更新。

也就是说，Eagle UI 有很多历史。在 Windows 3.1 之前就有了。有些人喜欢它，对一个心爱的程序的 UI 的任何改变都会通过窗口遇到砖头。不过，稍微调整一下不会有什么坏处，键盘快捷键是一个明显的附加功能。

### 欧特克的未来设计之旅

欧特克对 Eagle 的收购并不是在真空中发生的。2014 年，欧特克收购了 [Circuits.io](https://circuits.io/) ，这是一款电子设计软件，与 Fritzing 一样，基于无焊试验板范式。尽管很容易与 Fritzing 比较，Circuits.io 有一些相当先进的功能，包括模拟试验电路板电路。这不是 SPICE 模拟，但你不能看着[这样的东西](https://circuits.io/circuits/2258116-star-trek-clock#breadboard)而看不到电子设计的未来。

Circuits.io、Tinkercad 和 Autodesk 的 123D 系列应用是他们在创客市场的玩法。是的，您可以设计一个简单的电路并让它发挥实际作用，但您不会用这些工具来实现 FPGA 或任何为 EMC 兼容性而设计的东西。

当谈到严重的业务，欧特克的电子设计软件组合一直严重缺乏。这是有原因的:Altium 已经研究这个问题几十年了，它仍然不完美。KiCad 已经到了可以投票的年龄了，还有问题。老鹰也快三十岁了。构建 EDA 套件和 PCB 设计软件很难，可能是软件开发中最难的一个领域。欧特克公司不能简单地旋转他们自己的电子设计软件，并期望它是好的。Eagle 已经在那里，Premier Farnell 正在出售产品，Autodesk 收购 Eagle 也不足为奇。

这次收购意味着整合到欧特克的其他产品中。你已经可以使用 Autodesk 产品建造一个六速变速器、一栋房子和一艘宇宙飞船。Eagle 的加入意味着你也可以构建一个信用卡大小的 ARM 开发板。前进的道路是将所有这些能力集成在一个屋檐下；你将能够设计便携式视频游戏控制台的电子设备，并利用该电路板文件，围绕它构建一个外壳。

### 就个人而言

我已经使用 Eagle 很多年了。我知道这是一个相当有限的工具，我也知道 KiCad。我知道我需要一个更好的电子设计工具。我问自己的问题是，“当我现在真正需要做的事情*是在 Eagle 中花一个小时设计一个简单的电路板时，我想花时间和精力去学习 KiCad 吗？”*

 *这就是人们不使用更好的软件包的原因:我了解 Eagle，在学习 KiCad 的时间里，我可以完成我正在做的项目，做一个三明治，打个盹，然后把我的板邮寄出去。是的，很懒，但是老鹰已经足够好了。

随着 Eagle 的新方向，我相信我再也不用学习 KiCad 了。Eagle 即将变得更好——真的很好——我迫不及待地想看到 Autodesk 旗下的第一个 Eagle 版本。*
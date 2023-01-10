# 将吉他踏板从概念带入生产

> 原文：<https://hackaday.com/2017/12/20/taking-a-guitar-pedal-from-concept-into-production/>

开始一个新项目是很有趣的，而且通常需要花很多时间来玩试验板和原型板，并尽一切努力让事情运转起来。仅仅是让一个项目达到那个功能点看起来就像是一个巨大的时间投资。但是，如果您想更进一步，将您的项目从原型变为生产就绪形式，该怎么办呢？这是我如何用 Grav-A 失真踏板实现的故事。

### 为什么要造踏板呢？

![](img/77a816ff429ddd32bde3555cdce49cab.png)

The author, shown here with bandmates.

很久以前，我发现自己面临一个选择。随着毕业的临近，我需要决定一旦我的工程学位准备就绪，我的人生该做什么。当时，直接走进 9-5 的想法并不特别有吸引力，我想回到乐队，再次表演。然而，我担心长期休假会对我的潜在职业生涯产生影响。就在那时，我想到了一个解决办法。我将开办自己的电子公司，为音乐家制造产品。

我尝试并参与了各种项目，有时和朋友一起，有时独自一人。在探索了各种各样的选择之后，我决定用一个简单的失真踏板作为起点。它们很简单，部件很便宜，而且你可以用很多方法来玩这个设计，创造出各种各样美妙的声音效果。该产品将被称为 Grav-A——我的新公司 Grav Corp .的第一款产品。

### 我喜欢一个设计组合在一起

我通过回顾过去开始了这段旅程，想起我在 18 岁的时候就尝试过这样的建造。我以前尝试的吉他踏板是一堆松散的电线，主要是用回收的零件和当时在迪克·史密斯电子公司(想想澳大利亚的 Radio Shack)可以买到的少量电位器组装而成的。

![](img/4d872e881e1d89772c413dd81c1c56cc.png)

This youthful experiment from years past looked like a pig and squealed like one, too.

有严重的噪音和接地问题，踏板只能断断续续地工作。我以此为灵感去做得更好，并投身于研究。

互联网是一个很好的资源，它不仅为我提供了现有踏板的示意图和指南，还为我提供了自己解决问题的最佳途径。我在这里学到了特别早的一课。人们通常会谴责音乐设备的高昂价格，理由是普通踏板只使用了少数廉价部件。从某些方面来说，这是对的，但它未能纵观全局。

一个商用吉他踏板可能依靠晶体管、运算放大器和少量的无源元件来创造声音，这些东西确实非常便宜。但踏板的零售价还必须涵盖机械部件，如插孔、开关和电位计，外壳，包括油漆和印刷，组装和运输所需的劳动力，还必须留有一些利润空间，以保持背后的业务运行。我很快意识到，在价格上击败更大的运营商是不可能的，尤其是如果你试图打造一个能够经得起一般巡回音乐家虐待的坚固踏板。

在找到一些[伟大的](http://www.generalguitargadgets.com/how-to-build-it/technical-help/articles/design-distortion/) [资源](http://www.muzique.com/lab/tone3.htm)后，我决定使用一个运算放大器增益级，带有一个大的套筒式音调旋钮，并添加了一个现场控制。具有中心关闭位置的 DPDT 开关提供三种不同的限幅二极管选项——在反馈环路中、输出到地或关闭。看着精品踏板市场的其余部分，我决定实现一个[真旁路脚踏开关](http://thehub.musiciansfriend.com/tech-tips/tech-tip-true-bypass-pedals-and-buffers)，虽然价格昂贵，但它可以确保踏板电路在关闭时与进入吉他放大器的信号完全隔离。我还选择尽可能使用 PCB 安装的电位计和插孔，这有助于快速组装，也是在外壳内定位电路板的一种方式。古老的 Hammond 1590BB 将作为外壳，由一家专门从事踏板零件小批量生产的美国网站进行喷漆和印刷。我在 OSHPark 做了 10 个可爱的紫色 PCB，然后做了踏板。

### 从原型到生产

![](img/d33794f5c7d140285001474d064b57ff.png)

Enclosure artwork underwent many revisions to get everything to line up just right.

原型很棒，在舞台上很适合我，但是建造起来太费时间，而且比我喜欢的还要脆弱。尤其令人震惊的是 DC 电源插孔，它不太适合定制加工的外壳。虽然我很喜欢这个踏板，并从朋友那里得到了很好的反馈，但我不能把它以目前的状态投放到市场上，因为它的部分不太合适，艺术作品也不太准确。另一个问题是，我使用的原始运算放大器 LM301 已经停产。当我接近发布时，我决定调整这些问题。

对于外壳，我决定换一个新的制造商。最初的制造商的支持很差，并且使用非常不准确的模板进行美术和加工。更糟糕的是，他们要求将组装好的电路板送到他们那里，以使外壳适合印刷电路板。起初，这听起来像是一个可靠的方法，但是制造“适合”的东西是很差的工程实践，并且每次我不得不为他们运送一个稍微修改过的板增加两周时间。我转到的制造商通过使用提供的图纸中的精确测量值来工作，箱子回来时非常完美。在我尝试之前，我从来没有意识到，为了让这样一款产品上的艺术品与内部组件以及旋钮和插孔等东西正确对齐，需要进行多少尝试和错误。彻底的痛苦，但一旦完成就有回报。

![](img/5c15f84cff500b3b8f4559817353a027.png)

It’s not exactly CAD, but this drawing enabled the manufacturer to accurately position all the holes on the enclosure. I didn’t enjoy working in inches.

就 DC 电源插孔而言，我决定改用机箱安装的插孔，以前我曾试图重新创建一个现代的大套筒式设置，其中 9 V 插孔是 PCB 安装的，并点击进入机箱中的矩形孔。这是一个重大的进步，因为它使外壳更容易组装，制造商发现钻一个圆孔比造一个矩形孔容易得多。

其他优化出现在第二次生产运行中。我将状态 LED 的电阻和削波二极管的开关都移到了 PCB 上。这大大减少了我不得不剥离和手动点对点焊接的电线数量。由于所有这些变化，我将每个踏板的生产时间从 2.5 小时减少到了 1.5 小时。

我也开始实施其他技术来加速生产。我会拿十块板，把它们都组装起来，然后把它们都焊接起来，再组装成箱子。分阶段分批操作使我能够清楚地专注于确保每个踏板之间尽可能少的差异，因为它们都在同一时间经历相同的生产步骤。

### 头痛

有踏板的预购意味着把它们推出去有时间压力，这意味着我一头扎进了有组织的混乱生产中。有些教训是我完全没有预料到的。

随着产量的增加，最大的问题是外观损坏。当你以超过 150 美元的价格出售一件精品时，人们希望收到的是完好无损的。我从小在父母的工作室里为自己做项目，我的工作方法是粗糙和现成的。很容易将工具掉落在外壳上，或将设备掉落在地上，造成凹痕、刮痕或油漆碎屑，从而毁坏成品。我试图重新处理这些有缺陷的案件的可怕任务，但除了几个幸运的成功，这一切都是徒劳的。这是一个很大的问题，因为算上运费的话，每个箱子的成本远远超过 25 美元。在处理这个问题太多次后，我改造了我的工作台，放下软泡沫塑料，小心地整理我的工具，以避免无意中损坏箱子。事实证明，在设置我的工作区域时采取一些措施对于减少这些问题非常有价值。

![](img/c04200e9601233438410e8fee6647dea.png)

The first ever Grav-A , serial G-001, sitting centre stage on my pedal board.

除此之外，运输是个大问题。由于在澳大利亚经营，我不得不支付大笔费用来进口定制和标准零件。这些运费加在一起，使得它很难在价格上与美国等国家的其他精品踏板制造商竞争，这些国家可以更便宜地获得部件和外壳。这也是客户方面的一个绊脚石，因为将踏板运出澳大利亚也要花费一大笔钱。

最后，包装和设计问题浮出水面。剪辑模式开关很脆弱，一小部分在运输过程中被损坏。开关会卡在盒子的侧面，当受到撞击时，轴会脱离位置。这导致了几次昂贵的退货和更换。

### 故事如何结束

最终，很明显，销售一个在地球上更遥远的地方制造的失真踏板将是一个很难维持的前景。这当然不是不可能，但吉他踏板市场充斥着成千上万的失真踏板，因此很难脱颖而出。

在完成预定和完成第二次大规模生产后，很明显踏板在投入的时间内没有产生大量的利润。我开始慢慢抛售我的最后一批股票，同时开发针对不同市场的第二种产品。第二次经历这个过程，我做好了充分准备，避免了第一次遇到的许多陷阱。

总的来说，我强烈推荐[将一个电子项目投入生产](https://www.youtube.com/watch?v=XEd9NGrFPk4)。这些技能最好通过实践来学习。如果是第一次，选择一个小的、可实现的、市场有需求的项目。以尽快获得现金流来支持你的运营为目标，看看它会把你带到哪里。当然，最重要的是，一定要享受旅程！

 [https://www.youtube.com/embed/XEd9NGrFPk4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XEd9NGrFPk4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

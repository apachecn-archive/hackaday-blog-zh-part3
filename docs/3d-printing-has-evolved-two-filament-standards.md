# 3D 打印已经发展出两种灯丝标准

> 原文：<https://hackaday.com/2015/09/29/3d-printing-has-evolved-two-filament-standards/>

我们远远超过了 RepRap 项目的全盛时期，Hackaday tip line 每周都没有看到多个 3D 打印机的 Kickstarters。某种程度上，这有点亏。本十年前五年出现的低成本 3D 打印机的快速发展将永远无法与之匹敌，从现在起，我们只会看到渐进式的改进，而不是第一台 Prusa、第一台 Printrbot 甚至 Makerbot Replicator 所采取的革命性步骤。

这并不意味着一切都是标准化的。仍然有足够的空间来争论 deltas 与 Cartesians，床在 Y 轴上移动与沿 Z 轴移动，以及许多其他细节，使当前的打印机如此多样化。这些小争论中有一个特别有趣:灯丝的直径。今天，你可以买到任何类型的塑料，任何颜色，两种尺寸:1.75 毫米和 3 毫米。想想就觉得很诡异。为什么灯丝制造商、热端制造商，甚至打印机制造商会决定支持同一种耗材的两种不同品种？答案是历史选择、工程权衡和 3D 打印机实际工作的绝对武断的结果的混合。

### 起初

虽然基于灯丝的 3D 打印机已经存在了 20 年，但这些机器非常昂贵，通常藏在大公司和大学的工程部门。直到艾德里安·鲍耶开始了 RepRap 项目，自制热端的时代才开始到来。

用任何现代的标准来衡量，这些热点都是可怕的。[热塑性塑料挤出机](http://reprap.org/wiki/RepRapOneDarwinThermoplastExtruder)由镍铬合金丝、JB Weld、Blu-tack、PTFE 杆、铜管和 M6 黄铜螺柱制成。与 [E3D V6](http://e3d-online.com/E3D-v6) 相比——一个全金属的热端，有一个加热筒，合理的热设计，可更换的喷嘴，令人惊讶的是第一个热端竟然工作了。

[![Five years of development: [Adrian Bowyer]'s Thermoplastic Extruder 2.0 (left) and the e3D V6 (right)](img/73ecbd545b9f4d71236082a735818df8.png)](https://hackaday.com/wp-content/uploads/2015/09/nozzles.png) 

五年发展历程:【阿德里安·鲍耶】的热塑性挤出机 2.0(左)和 e3D V6(右)来源: [1](http://reprap.org/mediawiimg/d/d6/ThermoplastExtruder_2_0-heater-winding-2.jpg) ， [2](http://e3d-online.com/E3D-v6/Metal-Only/v6-1.75mm-Universal-Metal-Only) 。尽管最初热端实验中的几乎所有东西都被重新设计和重新制作，但有一件事仍然存在:3 毫米灯丝标准。第一台热塑性塑料挤出机被设计为接受 3 毫米细丝，细丝供应商的首批 [RepRap wiki 页面之一证实了这一点](http://reprap.org/mediawiki/index.php?title=Printing_Material_Suppliers&oldid=17613)。一切都是 3 毫米，Makerbot 在五年内将灯丝价格翻了一番。这里没有惊喜。3mm 灯丝一直是标准，直到 2011 年，1.75mm [登场，开始接管](http://reprap.org/mediawiki/index.php?title=Printing_Material_Suppliers&oldid=44477)。

### 为什么要换？

![Wade's Geared Extruder [Image Source]](img/3b1d71401fa147ca0e49a8387691c1db.png)

韦德的齿轮挤压机[图片来源](http://reprap.org/wiki/Wade's_Geared_Extruder)

最早的家用 3D 打印机几乎完全使用齿轮挤压机来推动细丝通过热喷嘴。这些齿轮挤压机，像[韦德的齿轮挤压机](http://reprap.org/wiki/Wade's_Geared_Extruder)，本质上是一个减速驱动。通过使用 1.75 毫米灯丝，步进电机所需的扭矩比使用 3 毫米灯丝少三倍。这种扭矩的减小意味着可以使用更小的直接驱动系统，并且由于驱动系统更小，整个打印轴的惯性减小。这意味着更小、更快的打印机也可以在较低的层高度打印得更好。

使用 1.75 毫米灯丝还有另一个优势——打印速度。加热质量越小，花费的时间就越少，如果你的目标是尽可能快地打印，你有两个选择:增加你向热端释放的功率，或者减小灯丝的尺寸。

这并不是说 3 毫米灯丝没有优势。如果你用大喷嘴或高速打印，你需要更大的细丝。当你认为某些东西像零件爸爸一样疯狂时，即使是最大的细丝也是不可能的；到那时，你就可以使用颗粒挤出机了。如果你使用鲍登设置，3 毫米灯丝将有点不耐弯曲，虽然。

1.75 毫米和 3 毫米灯丝之间的差异只是工程权衡中的一个选择——没有一个更好，但每个都有一些优势。

### 时势

尽管有一些像 Lulzbot 这样的坚持者，整个 3D 打印行业似乎已经决定采用 1.75 毫米的灯丝。新款 Printrbots 独家 1.75mm，Makerbots 使用 1.75mm 灯丝。Dremel Idea Builder 3D 打印机——在 Lowes 和 Home Depot 有售——使用 1.75 毫米的灯丝。如果你发现自己在接下来的一个小时内需要购买灯丝，你最好希望你的机器需要 1.75 毫米灯丝。

用一个设计好的打印机，1.75 和 3mm 的灯丝没有太大区别。一台经过适当调整的打印机可以用任何一种尺寸的灯丝生产出质量相似的零件。如果是这样的话，那么市场肯定会标准化这种或那种细丝，对吗？

这个看似显而易见的结果并非如此。在与一些灯丝制造商和经销商交谈中，1.75 毫米和 3 毫米灯丝之间的销量大致相当。出于这样或那样的原因，整个社区已经确定了两种不同的标准。

虽然这两种不同尺寸的打印机灯丝存在完全任意的演变，但实际上*并不重要*。设计打印机使用任何一种灯丝的工程选择都很简单，大多数人手头都会有足够的灯丝，这样他们就不必花 12 个小时跑到商店去打印 16 个小时。不过，有趣的是，我们怎么会对本应是一个标准的东西有两种完全不同的标准。
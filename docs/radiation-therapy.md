# 治愈物理学:放射疗法

> 原文：<https://hackaday.com/2017/12/04/radiation-therapy/>

没有几天比听到“对不起，你得了癌症”这样的话更糟糕了。当你得知这个消息时，对未知的恐惧、对疼痛的恐惧和对死亡的恐惧都会随之而来，没有什么能让你准备好应对身体背叛你的震惊。很难知道你体内有什么不应该存在的东西在生长，并且想把它取出来的冲动是压倒一切的。

有时有手术选择，有时没有。但是根除肿瘤并不总是外科医生的工作。高达 60%的癌症患者将接受某种放射治疗，通常与手术和化疗相配合。放射疗法可能会让一些人感到困惑——毕竟，难道辐射不会导致癌症吗？但是现代放射治疗是一个非常精确的过程，可以选择性地杀死肿瘤细胞，同时不伤害正常组织，我们为完成这项工作而建造的机器是一种迷人的工具，它结合了生物学和工程学，帮助人们应对可怕的诊断。

### 受控杀戮

简单地说，放射疗法是应用特定种类的电离辐射来治疗疾病，通常是癌症，但不总是癌症。这与使用辐射来收集诊断信息有本质上的区别，例如医用 X 射线、CT 扫描和核医学。所有电离辐射都有可能导致细胞损伤，但在诊断放射学中，剂量被保持在尽可能低的水平，以防止细胞损伤，同时仍能获得所需的诊断信息。然而，放射疗法使用一定剂量的电离辐射，其明确意图是以尽可能可控的方式杀死细胞。

为了理解放射疗法的工作原理，了解一些关于癌症的简单事实是很重要的。当然，癌症不是一种疾病，但是所有的癌症都有一个共同的特点:不受控制的细胞生长。癌细胞或多或少地不断分裂和增殖，经常形成称为肿瘤的实体块。癌细胞也往往是相对未分化的细胞；也就是说，它们缺乏正常细胞的特殊结构和功能。

这些特征提供了可用于治疗的弱点。细胞要分裂，就必须复制自己的 DNA，而 DNA 在复制的过程中，特别容易受到损伤。损伤可能来自于强力药物，如用于化疗的药物，或者细胞暴露于电离辐射。对细胞的损伤足够大，它就会死亡。破坏足够多的细胞，肿瘤开始缩小。

癌细胞更容易受到药物和辐射的损害，因为它们比周围的正常细胞复制得更快。但是正常细胞也在复制，当肿瘤细胞成为目标时，会造成附带损害。能够在杀死肿瘤的同时保护周围组织免受损伤是任何癌症治疗的目标，这也是放射疗法的亮点。

### 高能

放射治疗的工作原理是形成非常精确成形的电离辐射束，该辐射束可以照射肿瘤而不暴露周围的组织。问题是，身体是三维结构，无论你将光束瞄准哪个方向，正常组织要么在肿瘤上方，要么在肿瘤下方，都会受到辐射。幸运的是，细胞对累积的辐射剂量很敏感，所以有可能从多个角度提供部分剂量，限制对肿瘤上下结构的损害。这是通过围绕肿瘤位于焦点的患者轴向精确旋转治疗波束来实现的。随着时间的推移，肿瘤积累了足够的剂量开始死亡，而周围的正常组织则幸免于致命剂量。

用于实施外部波束放射治疗的机器可能非常复杂。它们不仅要产生极其强大的电离辐射束，还要控制、过滤和整形辐射束。他们还必须极其精确地定位射束，以便正确执行放射肿瘤学家和医学物理学家制定的治疗计划。最重要的是，机器必须有多层冗余的安全联锁，以保护病人和技术人员免受潜在的致命暴露。

电离辐射源的选择各不相同，不同的辐射源根据其产生的光子能量提供不同的治疗选择。*正电压 X 射线机*本质上是高功率 X 射线管，产生 200 到 500 千电子伏(keV)范围的束能量。像[诊断 X 射线管](http://hackaday.com/2016/05/12/to-see-within-making-medical-x-rays/)一样，正电压 X 射线管的工作原理是将电子加速到钨靶中，产生强大的光子束。

 [https://www.youtube.com/embed/jSgnWfbEx1A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jSgnWfbEx1A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在能量尺度上更高的是*线性加速器*机器，或者直线加速器。这些可以提供 4 到 25 兆电子伏特(MeV)范围的 X 射线束或电子束。在诊断和正电压 X 射线管中的电子源通常是简单的热阴极设计的情况下，直线加速器电子束是通过将电子从钨丝注入长波导管中而产生的。磁控管在波导管内产生射频驻波，将电子加速到巨大的动能。电子束可以直接使用，或者电子束可以用来撞击钨靶以产生高能 X 射线束。

### 保持身材

放射治疗机器最有趣的部分之一是准直器。准直控制光束的形状，限制不必要的曝光。诊断 X 射线机的准直器很简单——两组彼此成 90°设置的铅或钨叶片可以移入或移出光束，并产生各种尺寸的矩形。放射治疗光束需要能够匹配肿瘤的不规则轮廓，因此使用了*多叶准直器* (MLC)。MLC 有大量的钨板，可以移入和移出光束，以控制其大小和形状。MLC 被设置为基于从某个角度看到的目标肿瘤的二维轮廓来投射波束，该二维轮廓随着波束围绕患者旋转而改变。

MLC 是高度工程化的机制。不仅每片叶子都必须精确定位以符合治疗计划，还必须沐浴在高能光子中。叶片必须互锁和重叠，这样叶片之间就不会有泄漏，但是不能让热膨胀堵塞叶片。叶片还必须足够薄，以使光束边缘的“像素化”最小化。

 [https://www.youtube.com/embed/Llxe9t8wwB0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Llxe9t8wwB0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



当然，这些并不是放射疗法的唯一治疗方式。一些外部射线疗法使用固定的放射性同位素源，如钴-60，而不是加速器，一些疗法使用粒子束，如质子，来杀死癌细胞。但是不管治疗背后的物理原理是什么，控制致命辐射束只杀死需要杀死的东西的工程是值得钦佩的。

[专题图片来源:[瓦里安医疗系统](https://www.varian.com/)
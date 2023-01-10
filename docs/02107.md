# 自举一个 Amiga 2000 图形卡，因为古董是昂贵的

> 原文：<https://hackaday.com/2016/04/18/bootstrapping-an-amiga-2000-graphics-card-because-vintage-is-pricey/>

如果今天你的桌子上有一台电脑，那么它很有可能是英特尔架构的，并且在某种程度上是 IBM PC 的后代。它可能在前面有一个苹果徽章，它可能运行 Linux 或 Windows，但在硬件方面，压倒性的可能性是它将成为英特尔单一文化的一部分。几十年前，虽然在 16 位和早期 32 位时代，你会发现更多的架构多样性。个人电脑和克隆产品中的 Intel 3-和 486、Macintosh、Commodore 和 Atari 平台中的 68000 系列、苹果 IIGS 中的 WDC 65C816 以及带有早期 ARM 处理器的 Acorn Archimedes 等等。

在 20 世纪 90 年代的艰难环境中，这些替代平台大多半途而废。苹果在回归的史蒂夫·乔布斯(Steve Jobs)的领导下得以复兴，雅达利(Atari)和康茂德(Commodore)在一系列令人困惑的收购中衰落，Acorn 分裂并失去了自己的身份，其处理器授权子公司继续为我们今天认为理所当然的大多数移动设备提供动力。

令人惊讶的是，当 16 位平台的创始人淡出人们的视线时，一些 16 位平台拒绝消亡。尤其是 Commodore 的 Amiga，它拥有新的操作系统版本、新的平台和社区支持的硬件升级。今天早上，我们得到了这种设备的消息，[卢卡斯·哈特曼]的 [MNT VA2000，一种用于 Amiga 2000 的图形卡，使用在 FPGA](https://github.com/mntmn/amiga2000-gfxcard) 上实现的 GPU。

Amiga 2000 是 20 世纪 80 年代后期的一个目标，一个 68000 的 Amiga 在一个大盒子里，有许多 Commodore 的“Zorro”格式的扩展卡插槽。虽然它的图形功能在 1987 年是最先进的，但在 20 世纪 90 年代开始显示出它们的年龄，如果你今天想使用它，你会发现它在除了最低分辨率之外的任何方面都很乏味。第三方显卡在上世纪 90 年代为他们生产，但那些幸存下来的售价令人眼红。[Lukas]决定通过创建自己的 Zorro 卡来解决这个问题，卡上有 Papilio Pro FPGA 开发板，携带 Xilinx Spartan 6 来完成繁重的工作。

他对这个项目的评论既全面又有趣地描述了他所面临的障碍，以及他是如何克服这些障碍的。它包括一些巧妙的想法，如使用 Amiga 本身作为逻辑分析器，并描述了一些死胡同和他在这一过程中犯下的错误。你可能不是一个 Amiga 爱好者，但即使如此，它也值得一读。

我们很高兴在 Hackaday 看到 Amiga 相关的项目。我们中的一些人自己甚至有不止一个 Amiga。过去，我们报道过不少 Amiga 的故事，包括[这台 A2000 仍然在运行一所学校的 HVAC 系统](http://hackaday.com/2015/07/23/this-little-amiga-still-runs-school-districts-hvac/)。如果你想尝试 Amiga 的体验，而没有复活古代硬件的痛苦，尽管我们想向你介绍我们对 [AROS 的报道，一个 Amiga OS](http://hackaday.com/2015/10/27/aros-run-an-amiga-os-like-its-1993/) 的开源重写。

via[迪安·马斯卡]
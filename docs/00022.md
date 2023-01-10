# 在 Hackaday 上开发的——这是一个徽章。不，是哈吉

> 原文：<https://hackaday.com/2015/10/26/developed-on-hackaday-its-a-badge-no-its-the-hadge/>

不久前，我们宣布了“在 Hackaday 上开发”系列下的一个新项目的开始，这是 Hackaday 社区的一个徽章。在它的核心，这个徽章是一个徽章互联网的单一节点。在每次使用该徽章的活动中，都会创建一个 Hackaday Sub-Etha 网状网络，每个徽章都能够发送和接收来自其他徽章佩戴者的消息。有一个 Sub-Etha 到互联网网关的计划，所以即使佩戴徽章的人在世界的另一边，他们仍然通过 HaDge 网络连接。

事情进展得很快，所以我想做一个快速总结，并与社区分享进展。首先，它有一个名字。HaDge 是 HackaDay 徽章的缩写。到目前为止，我们的目标是建立一个团队，命名项目，建立存储库，并锁定一个工作材料清单。几周之内，我们就能搞定这一切。 [HaDge 群组聊天频道](https://hackaday.io/messages#/conversation/7968)非常活跃，每个人都提出了想法和建议。一个[电子表格](https://docs.google.com/spreadsheets/d/1TQAMLQUpt3ODg-VV_vUpoy4Eo5H531MVdNZf-1rAA8g/edit?usp=sharing)看起来是个好主意——它让每个人都可以添加他们关于候选零件的建议，创建一个功能列表，然后在频道上谈论它。

我们很早就意识到构建硬件需要一些时间。因此，在此期间，我们需要一个开发工具包平台，让软件开发人员能够着手开发为 HaDge 提供动力的智能产品。[Michele Perla]已经构建了 [JACK(只是另一个 Cortex 套件)](https://hackaday.io/project/6062-jack)——一个由 Atmel SAM D21 驱动的开发套件。它非常简单，只有最少的部件来使它工作，同时保持可靠性。HaDge 上的微控制器+无线电是 Atmel SAM R21-D21 的近亲，因此重新连接插孔并创建 [HACK (Hackaday Cortex kit)](https://hackaday.io/project/8007-hack) 是有意义的，这是一个由 Atmel SAM R21 驱动的开发套件，将用作 HaDge 的核心。[Michele]单枪匹马努力完成了设计，现在已经准备好很快进行 PCB 制造。我们只是在等待一些反馈和设计的天线部分的审查。我们硬件团队中没有人有强大的 RF-fu，所以我们不想犯一个可以避免的错误。如果你想回顾并帮助审查黑客设计，从 [github repo](https://github.com/MickMad/HACK) 获取设计文件并告诉我们。

一旦 HACK board 布局被清除用于制造，我们将致力于构建可以发送给软件人员的工具包。我们还将致力于将黑客设计移植到 KiCad，这是我已经开始的工作。我首先使用了由[LachlanA]开发的 neat [Eagle2KiCad 转换工具](https://github.com/lachlanA/eagle-to-kicad)。它并不完美，但确实减少了从 Eagle 移植到 Kicad 的工作量。一旦完成，实际 HaDge 的硬件开发将会看到一些进展——请关注项目页面。
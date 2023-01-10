# 取消特别提款权！

> 原文：<https://hackaday.com/2017/10/29/scratch-that-sdr/>

当您想到软件定义无线电时，您可能会考虑使用哪种语言来创建等式的软件部分？c？可能是 C++？

Scratch 怎么样？

"什么，Scratch 是针对年轻人的可视化编程语言吗？"，我们听到你怀疑地哭泣。这并不完全是你对 SDR 的期望，但由于[Andrew Back]的工作[，现在有了 ScratchRadio，这是软件定义无线电](https://www.crowdsupply.com/lime-micro/limesdr-mini/updates/raspberry-pi-3-and-scratch-demo)的一组临时扩展。究竟为什么要这样做？我们的目标是尽可能降低软件无线电的准入门槛，并将其置于一个学习环境中，如 Scratch，这似乎是实现这一目标的理想方式。

当然，Scratch 本身对于最繁重的工作来说不够强大，所以实际上这是一个用于 LuaRadio 后端的 Scratch 包装器。它是在考虑 LimeSDR Mini 的情况下创建的，但鉴于 LuaRadio 并不特定于该硬件，我们预计它可以与其他 SDR 一起工作，如一直流行的 RTL 芯片组电视棒。它让 Raspberry Pi 3 的所有者能够在不需要大量经验的情况下试验 SDR 编码，这对我们来说只能是一件好事。

如果你喜欢尝试 ScratchRadio，你可以在它的 GitHub 库中找到代码[，并从那里获得它。同时](https://github.com/myriadrf/ScratchRadio)[我们去年报道过 Lua Radio](https://hackaday.com/2016/07/06/luaradio-brings-more-options-to-sdr/)，所以如果 Scratch 对你来说有点基础，而 GNU Radio 又太高级，那就试试吧。

电台图标:【樱木博】，( [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Radio-icon.svg) )。

刮刮猫 logo: [麻省理工学院媒体实验室](https://scratch.mit.edu/terms_of_use/)。
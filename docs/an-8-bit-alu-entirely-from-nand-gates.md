# 一个 8 位 ALU，完全来自与非门

> 原文：<https://hackaday.com/2018/03/31/an-8-bit-alu-entirely-from-nand-gates/>

每个学数字电子学的学生都知道的一件事是，每一个逻辑功能都可以由与非门组合而成。但是没有人有足够的胆量去尝试一下，毕竟那需要非常多的门！

显然有人忘了告诉[Notbookies]，因为[他在一组试验板上仅用 4011B 四路与非门](https://hobbyundecided.wordpress.com/2018/01/28/an-8-bit-alu-made-entirely-out-of-nand-gates/)就制作了一个完整的 8 位 ALU，并在这样做的过程中用他的布线制作了一个小杰作。它的灵感来自[【食本】](https://www.youtube.com/playlist?list=PLowKtXNTBypGqImE405J2565dvjafglHU)的一系列视频，描述了一台采用所谓的 SAP(尽可能简单)架构的计算机的构造。48 个 4011B DIP 封装位于 8 个标准试验板上，另外一个用于一组 DIP 开关和 led，一组电源母线试验板位于其侧面。他留给我们的建议来自痛苦的经历:“*除非你的目标是建造一台只支持 NAND 的计算机，否则就选择最适合这项工作的集成电路*”。

这些年来，我们已经讨论了无数由分立逻辑芯片制造的处理器和处理器组件，尽管这并没有降低它们令人印象深刻的成就。[nedo NAND 是最近的一个例子](https://hackaday.com/2016/02/24/8-bit-computer-made-solely-from-nand-gates/)，它是一种基于 PCB 的模块化设计。TTL 和 CMOS 逻辑芯片在 50 多年前首次亮相，所以你可能会认为这个方向没有什么新的东西，但是我们认为这是一个很好的项目，将会持续很多年。

通过[/r/电子/](https://www.reddit.com/r/electronics/comments/870wj0/8bit_alu_made_using_only_quadnand_ics/) 。
# 奇怪的 CPU

> 原文：<https://hackaday.com/2016/08/06/weird-cpu/>

【agp.cooper 的】[电脑](https://hackaday.io/project/12879-weird-cpu)有多少条指令？只有一个。它用了多少长条纸板？显然， ~~41~~ 五块 41 轨道板。虽然是一个害羞的生活的答案，它仍然是一个单一的指令很多板。电路板数量多是因为使用了 20 世纪 70 年代的老式 IC，包括 TTL 器件、2114 RAM 芯片和 74S571 PROMs。

单指令计算机有几种不同的体系结构，agp 使用 TTA 的技术(传输触发体系结构)。也就是说，一条指令是一次移动，移动的目的地或来源决定了操作。例如，Wierd CPU(这是它的名字)有一个 P 和 Q 寄存器。如果你加载这些寄存器，那么加法寄存器将包含两个数的和。

功能单元(像 ADD)也不多。有一些跳转，一些 I/O，你可以做一个 NAND 或 ADD 操作。我们不怪他这么大量的板和零件都很节约。然而，如果你跳跃到 FPGA，你可以建立一个[更强大的单指令机器](http://www.drdobbs.com/embedded-systems/the-one-instruction-wonder/221800122)。然而，我们已经涵盖了许多其他的 one instruction 奇迹，包括可试验的 [DUO Compact](https://hackaday.com/2012/09/05/mess-of-wires-is-actually-a-one-instruction-computer/) 和 [SUBLEQ-OISC](https://hackaday.com/2011/07/27/building-a-one-instruction-computer/) 。
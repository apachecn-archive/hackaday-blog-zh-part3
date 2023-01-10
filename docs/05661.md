# TTL 中的 8 位传输触发结构 CPU

> 原文：<https://hackaday.com/2017/04/21/an-8-bit-transport-triggered-architecture-cpu-in-ttl/>

当向我们介绍微处理器的内部结构时，我们很可能会看到类似于 20 世纪 70 年代第一代 8 位 CPU 的东西。将会有一组熟悉的寄存器和计数器、一个算术和逻辑单元(ALU)以及一个带有相关控制逻辑的指令解码器。一个复杂的指令集使得解码器能够安排寄存器和 ALU 以正确的顺序执行各种功能。自 20 世纪 70 年代以来，CPU 可能在许多方面都有所发展，但 8080 或类似产品的框图仍然为初学者提供了基本的基础。

因此，当我们告诉你另一个使用 TTL 逻辑芯片的国产 CPU 时，你可能会认为它会遵循这条老路。幸运的是，硬件黑客社区总是能够给我们带来惊喜，而[Szoftveres]已经用他的设计做到了这一点。它是[遵循传输触发架构](https://hackaday.io/project/11703-8-bit-ttl-cpu)的单指令集机器，这意味着它与上面描述的传统架构有很大不同。每条指令都是处理器不同物理功能之间的一次移动，计算是由物理功能在数据移入它们时对数据进行处理，并在它们的输出上呈现结果，以备移动到其他地方。结果是一台计算机以其自己的方式非常简单，尽管代价是一些不灵活和缺乏一些我们在更传统的处理器中认为理所当然的硬件功能。

这台机器是建立在一块条形板上的，有一块附带的板，板上有显示器、键盘和调制解调器。有一个基于 ATmega8 微控制器的小型板，它执行快速程序加载的功能，一旦加载了代码就可以移除。软件可以用类似 C 语言的语言编写，并使用他的 GitHub 库中的编译器[进行编译，他已经制作了一个机器运行的 YouTube 视频。这个项目非常值得深入阅读，因为它介绍了这个有点不寻常的架构。](https://github.com/szoftveres/ttlcpu)

 [https://www.youtube.com/embed/Y3wZ4TLqmI8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y3wZ4TLqmI8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这些年来，我们为您带来了无数的 74 个 TTL 逻辑 CPU，但令人惊讶的是[这不是第一个单指令设计](http://hackaday.com/2016/06/11/designing-a-single-instruction-computer/)。
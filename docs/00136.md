# 入侵 2.4GHz 无线电控制

> 原文：<https://hackaday.com/2015/09/20/hacking-2-4ghz-radio-control/>

许多现代无线电控制(RC)系统使用跳频来防止干扰。不幸的是，在 2.4GHz 频段上跳来跳去会干扰使用相同频段的视频或 WiFi。当[Befinitiv]意识到大多数系统使用 TI CC2500 芯片和微控制器时，他正试图解决这个问题。微控制器通过 SPI 命令芯片，并通过写入频率寄存器来控制频率。

更新微控制器固件是不切实际的。首先，固件是加密的。此外，必须在任何未来的更新中重新插入更改，并为每个 RC 供应商重复进行。所以[Befinitiv]采取了不同的方法。他做了一个典型的中间人攻击，在控制器和 CC2500 之间插入 CPLD。

简单来说，CPLD 就是一个小型 FPGA。通常存在一些内部架构差异，但是您可以像配置 FPGA 一样使用 Verilog 或 VHDL 来配置它们。[Befinitiv]所做的是监控 SPI 时钟线并拦截数据线。对于大多数操作，CPLD 只是传递数据。然而，当它看到通道寄存器写入时，它会动态改变数据。正如你所料，这是对时序敏感的，这也是他使用可编程逻辑器件而不是微控制器的原因。

当然，发射机和接收机都需要修改。无论软件如何变化，该系统都可以继续工作，甚至可以在其他基于 CC2500 的系统上工作。

这当然没有我们上一次讨论的 CC2500 黑客攻击生动。然而，这是一件很好的作品。即使你目前的设置没有使用 CC2500，你也可以修改它(见下面的视频)。

 [https://www.youtube.com/embed/0oXjk_oQsE8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0oXjk_oQsE8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[lageos]的提示。
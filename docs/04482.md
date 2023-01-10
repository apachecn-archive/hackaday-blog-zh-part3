# 微型 SCSI 模拟器

> 原文：<https://hackaday.com/2016/12/25/the-tiny-scsi-emulator/>

对于 80 年代和 90 年代的老式电脑爱好者来说，SCSI 可能是一个真正的眼中钉。可用硬盘的存量正在减少，神秘的终止问题肯定会让你在不久后诅咒 SCSI 巫毒。多年来，这导致了各种项目，旨在创造新的 SCSI 硬件，以填补原始设备太坏而无法使用或太罕见而无法找到的地方。

[David Kuder]的[微型 SCSI 模拟器](https://hackaday.io/project/18974-tiny-scsi-emulator)就是为此而设计的。[David]将 Teensy 3.5 与 NCR5380 SCSI 接口芯片相结合来构建他的设备。凭借 120MHz 的时钟和 192K 的 RAM，Teensy 提供了足够的马力来跟上 SCSI 信号，其 DMA 功能也不会受到影响。

现在，许多早期的 SCSI 仿真或转换项目纯粹专注于存储，例如 [SCSI2SD](http://www.nekochan.net/wiki/SCSI2SD) ，它使用 microSD 卡来仿真 SCSI 硬盘驱动器进行存储。[David]做到了这一点，最大限度地提高了 NCR5380 的吞吐量，并在 SD 卡方面留出了大量空间。未来的工作希望通过 SCSI 控制器升级获得更高的速度。

但这并不是 SCSI 的全部优势。回到 80 年代的野蛮时代，许多电脑，尤其是早期的 Macintosh 系列，缺少扩展选项。这导致了 SCSI 以太网适配器的开发，[David]也试图通过在他的项目中添加 W5100 以太网屏蔽来进行模仿。到目前为止,[David]使用的 Cabletron EA412 驱动程序导致 Macintosh SE 测试系统在初始设置后崩溃，但调试仍在继续。

看到旨在保留老式硬件的项目总是很棒——就像这个[大规模修复六个 Commodore 64](http://hackaday.com/2016/08/07/detailed-log-of-commodore-64-refurbishing/)。
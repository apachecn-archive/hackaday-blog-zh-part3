# 压制英特尔的管理引擎

> 原文：<https://hackaday.com/2016/11/28/neutralizing-intels-management-engine/>

大约五年前，英特尔推出了一些可怕的东西。英特尔的管理引擎(ME)是一个完全独立的计算环境，运行在英特尔芯片组上，可以访问一切。ME 可以访问网络、访问主机操作系统、内存和加密引擎。即使电脑关机，也可以远程使用 ME。如果这听起来很可怕，情况会变得更糟:没有人知道 ME 在做什么，[我们甚至不能看代码](http://hackaday.com/2016/01/22/the-trouble-with-intels-management-engine/)。当——而不是“如果”——ME 最终被破解时，每台运行最新英特尔芯片的计算机都将面临巨大的安全和隐私问题。英特尔的管理引擎是有史以来最危险的计算机硬件。

研究人员正在继续破译 ME 的内部工作机制，我们真诚地希望这个潘多拉魔盒保持关闭。在那之前，[现在有一种新的方法来禁用英特尔的管理引擎](http://hardenedlinux.org/firmware/2016/11/17/neutralize_ME_firmware_on_sandybridge_and_ivybridge.html)。

以前，GM45 芯片组中的 ME 的第一次迭代[可以被移除](https://libreboot.org/docs/hcl/gm45_remove_me.html)。这种技术是因为 ME 位于与北桥分离的芯片上。对于酷睿 i3/i5/i7 处理器，ME 集成到北桥。到目前为止，禁用与 CPU 紧密耦合的 ME 的努力都失败了。从这些系统中完全移除 ME 是不可能的，但是禁用 ME 的某些部分是可能的。有一个警告:如果 ME 的启动 ROM(存储在 SPI 闪存中)没有找到有效的英特尔签名，PC 将在 30 分钟后关闭。

几个月前，[Trammell Hudson]发现擦除 ME 区域的第一页并没有在 30 分钟后关闭他的 Thinkpad。这导致[尼古拉·索蕾娜]和[弗雷德里克·阿米迪欧·伊佐]写了一个利用这个漏洞的脚本。实际上，ME 仍然认为它在运行，但它实际上不做任何事情。

有了一个比格犬骨，一个 SOIC-8 芯片夹，和一些突破线，这个脚本将运行并有效地禁用 ME。此漏洞仅被确认在 Sandy Bridge 和 Ivy Bridge 处理器上有效。它应该可以在 Skylake 处理器上工作，Haswell 和 Broadwell 尚未经过测试。

将 ME 从 CPU 中分离或禁用一直是 libreboot 和 coreboot 社区关注的焦点。迄今为止，无法做到这一点使得真正自由的计算平台前景黯淡。万物皆有我，没有我的 CPU 正在老化。即使我们没有能力移除 ME，禁用它也是退而求其次的选择。
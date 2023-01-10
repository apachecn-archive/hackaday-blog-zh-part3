# 运动控制 KVM 开关

> 原文：<https://hackaday.com/2018/04/16/motion-controlled-kvm-switch/>

很久以前，[hardwarecoder]获得了一台 Gen8 HP 微服务器，并开始摆弄它。它从“尝试”一些可视化开始，然后脱离正轨，用 ZFS 作为 QEMU-KVM 虚拟机完全设置 FreeBSD。当他不知道下一步该做什么时，他碰巧感叹他不能把笔记本电脑放在他的桌子上，所以他给自己做了一个光滑的运动感应 KVM 开关来解决他的空间问题。

其核心是，该设备通过显示器 VGA 电缆上的 I2C 引脚注入 DCC 代码来交换输入，同时继电器将键盘和鼠标从服务器“重新插入”笔记本电脑，反之亦然。在完全定制的 PCB 上有一对红外二极管和一个接收器，它可以检测激活交换的绝地武士般的手波。它比某些方法稍微复杂一点[，但是可以说**比**酷得多。](https://hackaday.com/2017/08/05/hackaday-prize-entry-low-cost-kvm/)

使用适配器，pcb 插入他的键盘，显示器数据连接和键盘/鼠标输出到笔记本电脑和服务器从那里流出。PCB 上的电缆有一个轻微的潜在问题，但由于它如此方便地靠近，[hardwarecoder]不需要太多处理它。

[hardwarecoder]的帖子是一个令人印象深刻的详细分类，并为那些敢于投入类似努力的人提供了指导。当管理较大的计算机系统时，KVM 交换机是方便的解决方案，但如果不加检查的话，可能会成为[潜在的漏洞](https://hackaday.com/2015/08/08/hacking-a-kvm-teach-a-keyboard-switch-to-spy/)。
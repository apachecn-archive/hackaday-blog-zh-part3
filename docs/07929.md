# 利用 SDRPlay 挖掘业余无线电的潜力

> 原文：<https://hackaday.com/2017/12/10/tapping-into-a-ham-radios-potential-with-sdrplay/>

软件定义的无线电是业余无线电操作员的伟大工具，允许大范围频谱的可视化，并让 hams 通过点击鼠标快速锁定微弱的信号。高端业余无线电通常内置这一功能，但通过使用 SDR 接入收发器的 RF 级[，即使预算有限的业余无线电也可以享受高端功能。](https://www.instructables.com/id/Yaesu-FT-450D-RF-Tap-Modification-for-SDR/)

UK ham [Dave (G7IYK)]在他的小屋中使用了坚固可靠的八重洲 FT-450D 和多功能 SDRPlay，寻找连接这两种设备的最佳方式。使用两个独立的天线是可能的，但不优雅，并且在两个设备之间切换 RF 路径似乎很笨拙。因此，他决定利用高阻抗低噪声放大器(LNA)接入收发器的 RF 级，并将输出馈入 SDRPlay。简单的 LNA 是建立在一个铣削的 PCB 上。稍微研究一下八重洲手册(ham radio gear 几乎总是包括原理图)，他就找到了 RF 路径中的正确抽头点，就在带通滤波器网络之前。这使得 SDRPlay 可以在中频级之前看到信号。他还确定了只有当无线电不发射时，LNA 号才能获得能源的可能点。LNA 在收音机里，SDRPlay 在外面，他现在有了一个瀑布显示器，多亏了 Omni-Rig 遥控软件，他可以点击鼠标调整八重洲。

如果你需要了解更多关于 SDRPlay 的知识，那么[【Al Williams】《GNU Radio 和 SDRPlay 指南》](https://hackaday.com/2015/11/12/your-first-gnu-radio-receiver-with-sdrplay/)是一个很好的起点。

 [https://www.youtube.com/embed/Eve88YqDlE8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Eve88YqDlE8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


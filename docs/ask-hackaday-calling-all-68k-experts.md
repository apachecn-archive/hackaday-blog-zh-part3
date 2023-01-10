# 问黑客日:召集所有 68k 专家

> 原文：<https://hackaday.com/2016/08/22/ask-hackaday-calling-all-68k-experts/>

这是一个关于旧 CPU、密集的 SMD 返工以及应该工作但没有工作的事情的故事。

1994 年发布的苹果 Powerbook 500 系列笔记本电脑是该系列的顶级产品。他们有内置的以太网、代替轨迹球的触控板、立体声音响和全尺寸键盘。这是第一批看起来像现代笔记本电脑的笔记本电脑之一。

这些笔记本电脑中的 CPU 除了高端的日本专用 Powerbook 550 c——是 68LC040。部件名称中的' *LC* '标志表示该 CPU 没有浮点单元。几个月前，[quarterturn]正在寻找一个项目，并决定更换 CPU 将是一次宝贵的学习经历。他从笔记本电脑上取下 CPU 卡，拿出一些芯片，重新制作了一个 180 针的 QFP 封装。[这并不顺利](http://hackaday.com/2016/02/24/upgrading-and-desoldering-a-fake-cpu/)。替换的 CPU 来自中国，即使新 CPU 上激光显示的数字是 68040，而不是 68 *LC* 040，[这台笔记本电脑仍然没有浮点单元](https://hackaday.io/project/9150-68040-upgrade-for-powerbook-520c/log/32305-not-fake)。尽管如此，这是一个令人印象深刻的返工能力的展示，并为消费电子历史的旁注产生了一个事实。

面对一台经过大量非常非常精细的焊接后实际上没有变化的笔记本电脑，[quarterturn]有两个选择。他可以把 Powerbook 放回零件箱，或者他可以采购一个带 FPU 的 68040 CPU。他选择了后者。新的芯片是飞思卡尔 MC68040FE33A。恩智浦支持代表保证，这款 CPU 确实有浮点单元，[quarterturn]检查了 Mac 的系统信息。没有列出 FPU。他安装了 NetBSD。[没有安装 FPU](https://hackaday.io/project/9150-68040-upgrade-for-powerbook-520c/log/43395-netbsd-shows-no-fpu)。这很奇怪，不应该发生，现在[quarterturn]已经达到了关于 Powerbook 500 架构的知识极限。因此，问问黑客:为什么这个 FPU 不工作？

[神圣的卷轴](http://www.nxp.com/files/32bit/doc/ref_manual/MC68040UM.pdf)从摩托罗拉到飞思卡尔再到恩智浦陈述了无 FPU 的 68LC040 和配备 FPU 的 68040 之间的一些差异。它们彼此引脚兼容，目标代码兼容(FPU 指令除外)，并且时序要求相同。这应该是一个下降的替代品。事实并非如此，也没有令人满意的解释说明为什么会这样。

诊断问题的第一步是排除可能的问题，在这种情况下，可能不是软件问题。CPU 报告在 Mac OS 和 NetBSD 中都没有 FPU。配备 FPU 的 Powerbook 550 已经存在，Mac OS 对整个 Powerbook 500 系列使用相同的[完形 ID](https://support.apple.com/kb/TA47453?viewlocale=en_US&locale=en_US) 。由于[quarterturn]在 NetBSD 下测试了 CPU，ROM 中可能也没有什么奇怪的事情发生；Mac ROMs 几乎完全专用于 Macintosh 工具箱和 Mac OS。问题可能不在于软件。

根据摩托罗拉、飞思卡尔和恩智浦的文件，问题可能不是硬件。这是这台电脑的第二个新 CPU，这次的 CPU 很可能有浮点单元。我们可以信任恩智浦支持代表，也可以信任在项目过程中多次返工的 PCB。如果它能与无 FPU 的 CPU 一起工作，那么它应该能与配有 FPU 的 CPU 一起工作。

没有一个显而易见的解决这个问题的软件，硬件，甚至这个笔记本电脑的 ROM，这个项目已经变成了一个谜。数据手册中肯定藏着一些勘误表，会告诉我们发生了什么。可能有少数干瘪的苹果工程师知道问题出在哪里。这个问题的解释将很难找到，这就是为什么这个项目是一个问答专栏。评论是公开的，最终的答案肯定会非常有趣。
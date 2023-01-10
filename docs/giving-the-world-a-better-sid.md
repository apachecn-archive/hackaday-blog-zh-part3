# 给世界一个更好的 SID

> 原文：<https://hackaday.com/2016/11/24/giving-the-world-a-better-sid/>

这里有一个商业计划给你，如果你曾经遇到一个坐在垃圾箱里的旧硅晶圆厂:建立准将 SID 芯片。MOS 6581 和 8580 是一个芯片上的合成器，著名地用于演示场景，甚至今天每个芯片的价格高达 40 美元。这是有市场的，通过正确的流程，这可能是一个可行的商业计划。

在垃圾箱里找到一个硅晶圆厂是一件遥遥无期的事情，但这里有一个最好的事情:[一个 FPGASID 项目](http://www.fpgasid.de/home)。该 FPGASID 是一个项目，以重新创造现在 unobtanium MOS 6581 发现的准将 64。

Commodore SID 芯片已经停产一段时间了，几乎所有可用的 SID 芯片都已经被建造 midi box SID T1 的人抢购一空，或者被 T2 Elektron 用于他们已经停产近十年的 SID station T3。对 SID 芯片的需求已经被“克隆”或使用 [ATmegas](http://www.roboterclub-freiburg.de/atmega_sound/atmegaSID.html) 、[螺旋桨](http://hackaday.com/2012/08/31/propeller-turned-into-chiptune-player-with-a-software-sid/)和几乎所有其他可用的微控制器架构的再创造所填补。虽然这些克隆体可以正确地获得 SID 的四个声音，但有一个普遍的问题:SID 有模拟滤波器，没有两个 SID 听起来是一样的。

从 FPGASID，项目页面上的[可用音频样本来看，滤波器可能是一个已解决的问题。FPGASID 的输出听起来*很像老式 SID 的输出。这是否是每个人都同意的 SID 听起来应该是另一回事，但这是迄今为止将 Commodore 64 芯片上的 synth 带入现代的最佳尝试。*](http://www.fpgasid.de/project-definition)

文件、固件和 FPGA 特殊酱还不可用，[但 FPGASID 正在 alpha 测试中](http://www.fpgasid.de/alpha-phase)，暂定于 2017 年初正式发布。也许现在是时候找出优步 MIDIbox 的那些计划了。
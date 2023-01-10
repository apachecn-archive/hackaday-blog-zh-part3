# 升级和拆焊假 CPU

> 原文：<https://hackaday.com/2016/02/24/upgrading-and-desoldering-a-fake-cpu/>

[quarterturn]的垃圾箱里放着一台旧的苹果 Powerbook 520c。当时，这是一台很棒的电脑，但从更现代的角度来看，它需要升级。它也不能运行 BSD:为此你需要一个 FPU，520 使用低成本、无 FPU 版本的 68040 作为主处理器。你可以直接从中国购买带 fpu 的 68040 版本，这意味着将这款旧 Powerbook 变成 BSD 发电站只需要拆焊和升级 CPU。这正是[quarterturn]所做的，遭遇了意想不到但并不令人惊讶的挫折。

Powerbook 500 系列的主板设计巧妙，带有用于 CPU 本身和 RAM 升级的子卡。从笔记本电脑上拔下 CPU 子卡后，[直角转弯]面对他的克星:一台 180 针的 QFP 68LC040。通过 ChipQuik 的自由应用，移除 CPU[相对容易。用焊料编织和一些助焊剂快速点击几下，一切都清理干净了，子卡已经为新的 CPU 做好了准备。](https://hackaday.io/project/9150-68040-upgrade-for-powerbook-520c/log/30449-680lc040-removal)

[配备 FPU 的新 CPU 来自中国](https://hackaday.io/project/9150-68040-upgrade-for-powerbook-520c/log/30827-68040-has-arrived)，经过非常仔细的检查、焊接和测试，【quarterturn】为他的 Powerbook 配备了一个新 CPU。Powerbook 恢复运行后，出现了一个小问题。[芯片是假的](https://hackaday.io/project/9150-68040-upgrade-for-powerbook-520c/log/32305-fake)。即使新的 CPU 被标记为 68040，它也没有 FPU。人们会伪造任何东西，包括 90 年代早期的处理器。这意味着没有 FPU，没有 BSD，而[quarterturn]实际上又回到了起点。

这并不意味着这次演习是一次彻底的失败。[quarterturn]确实从这次经历中学到了一些东西。事实上，你可以用 ChipQuik 去焊接一个致密的 QFP，也可以用普通的烙铁焊接同一个芯片。跨越 20 年的麦金塔操作系统的联网是一团乱麻，而且*买者自负*也不能翻译成普通话。
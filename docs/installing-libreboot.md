# 在 ThinkPad 上安装 Libreboot 的悲惨故事

> 原文：<https://hackaday.com/2016/12/16/installing-libreboot/>

作为一名苹果用户，在过去的几年里，我变得有些失望。也许是史蒂夫·乔布斯的精神正在慢慢从公司消失，或者是苹果似乎更关心最近的昂贵趋势而不是引领它们，或者是苹果没有把我作为用户的最大利益放在心上。

不管是什么，我一直在被动地寻找一台新的笔记本电脑，幻想着有一天我可以扔掉我的苹果，换一台更好的。它可以运行某种*nix 操作系统，由高质量的硬件制成，并且不会让我担心隐私问题。我认为笔记本电脑根本不具备这些品质，我的 2012 款 MacBook Pro 是“两害相权取其轻”，我还不如继续使用。但是后来，我们发表了一篇 ThinkPad 的思考文章，其中有两个词，引导我开始了一个长达数周的旅程，来到我目前正在使用的全新的、使用了八年的笔记本电脑前。那两个字:“安装 libreboot”。

Libreboot 是一款免费软件，可以取代一些现代电脑上的专有 BIOS 固件。令人惊讶的是，随着英特尔加快部署英特尔管理引擎，这变得越来越困难。简而言之，IME 是一个独立的处理器，可以监控甚至接管计算机中发生的一切，并通过网络将信息发送给任何拥有控制权的人(或任何公司)。它在用户不知情的情况下这样做，并且(显然)是一个巨大的安全漏洞。由于英特尔的竞争对手也在做类似的事情，除非你能用 libreboot 或 [coreboot](https://www.coreboot.org/) 之类的东西取代 IME，否则几乎没有逃脱的可能。

## 没你想的那么简单

当我开始研究 libreboot 时，我以为这是一个简单的过程:下载它，在我的电脑上运行一些安装程序，刷新 BIOS。不会超过半小时的！特别是因为最初的文章只是简单地说“安装 libreboot ”,好像这是一个孩子在午睡之间可以做的事情。然而，我即将投入的现实却大不相同。

首先，libreboot 只能在少数旧款 ThinkPads 上运行。新型号已经成为英特尔新策略的受害者，该策略检查 BIOS 芯片上加载的固件，如果发现未经批准的固件，则禁用计算机。显然，英特尔认为修复安全缺陷或修改您拥有的东西是荒谬和不可接受的。不管怎样，我在易贝用 65 美元的运费买了一辆 8 年前的 X200。我是一个简单的人，喜欢简单但可靠的东西，即使他们已经相处多年了，所以电脑的年龄对我来说不是太大的问题。我觉得自己做得很好，于是看了看新固件的安装说明。

## 需要一些拆卸

这是我在订购电脑之前应该采取的一个步骤。这并不会阻止我这样做，但它可能会让我更好地了解我应该从这个过程中期待什么。首先，我发现要闪存芯片，需要拆卸和焊接。固件必须直接编程*。任何时候像这样的事情被做，砖设备是一个真正的可能性。至少我只会损失 65 美元。*

[![](img/fe8c4606a6260d3c15e455672dd8a906.png)](https://hackaday.com/wp-content/uploads/2016/12/img_1037.jpg)

The tiny chip to the left of the Intel-branded processor is the source of the problem.

然后，我了解到 BeagleBone Black 是用来将新固件刷新到 ThinkPad 的首选设备。我有三个树莓馅饼，但我还是可疑地花了 40 美元点了一个比格犬骨。不会有坏处，我告诉自己，将来我会有一个新工具来做其他事情。但是看起来很奇怪，没有使用树莓派的选项。

下一个障碍是弄清楚我的笔记本电脑中的固件芯片到底是什么类型的，因为不同类型的芯片有不同的 [SOIC](https://en.wikipedia.org/wiki/Small_Outline_Integrated_Circuit) 夹子，而要弄清楚我有哪种尺寸的芯片，唯一的方法就是拿到笔记本电脑并把它拆开。这让我花了几天时间(又花了 10 美元)等待正确的剪辑。在这个过程中，我还了解到，没有免费软件可以在这些电脑的英特尔专有 WiFi 卡上运行，所以我也订购了一个 Atheros 卡来安装(15 美元)，因为我已经把笔记本电脑拆开了。

![img_1044](img/1fadc5d5e359176168cd0907298d7e70.png)

New Atheros WiFi card installed.

接下来，比格骨必须以一种非常特殊的方式进行配置。我以前从未接触过这些，它不像树莓派那么简单。这个过程花了我两天中的几个小时。我还通过第三方教程了解到[Libreboot 实际上*可以*用树莓 Pi 刷新，但这是(许多)libre boot 人员尽可能使用免费开源软件的情况之一。比格犬骨符合他们的要求，Pi 不符合，他们也没有提到这一点。我本可以很容易地为自己省下 40 美元，并使用 Pi，但本着 libreboot 的精神(以及我已经走得太远而无法切换的事实)，我坚持了下来。](https://iqlusion.org/index.php/2016/03/01/x200-libreboot/)

## 导航 Libreboot 的安装过程

我在设置 BeagleBone 时遇到的最大问题是 libreboot 的文件和[指令](https://libreboot.org/docs/install/x200_external.html#clip)。例如，有一次我不得不用一个特定于我笔记本电脑中以太网卡的 MAC 地址描述符来修补 libreboot ROM 文件。目前还不清楚提供的众多脚本中哪一个会这样做。即使在那时，不同的 rom 都在一个文件夹中，除非你马上意识到这一点，否则当你解压文件时，你会填满 BeagleBone 的内存。总的来说，我觉得我需要多个计算机科学学位才能在第一次尝试时理解他们的指令。这可能是自由软件的通病:通过与那些知识和经验较少的人无关的文档来疏远人们。我也不是业余爱好者。我有电气工程学位，对正在发生的事情也略知一二，但即便如此，我还是觉得自己在一片黑暗的术语丛林中盲目前行。

反正我收到的 BeagleBone Black 没有显示输出(我能找到的；我以前从未使用过，可能会遗漏一些东西)，我很难通过 USB 连接到我的 Mac 上。这意味着通过以太网把它接入网络，因为我的路由器在厨房里，所以我在那里开了家店。在将一些电线焊接到 SOC 芯片后，我终于准备好开始刷新一些固件了。在这一点上，我拥有 X200 已经快三个星期了，所有的时间都花在了等待我不可能知道我需要的部件上，以及作为一名程序员对 BeagleBone 进行编程。

![img_1042](img/e056755dc7960b0ca6734d29ff72a336.png)

My libreboot flashing station in the kitchen. Complete with janky power supply.

不过，实际的闪光只花了我大约一个半小时。一旦我弄清楚使用哪种 ROM 并连接上我的 3.3V 电源(幸运的是我已经有了一个这样的电源)备份出厂 ROM、验证它并开始刷新 libreboot 是一个相当简单的过程。不过，在这一点上有一个大问题。我尝试了这个过程四次，每次都无法验证新固件。错误消息到处出现，这是您在流程的这一点上不希望看到的。BeagleBone 成功地编写了固件，但后来，出于某种原因，无法验证它。做完这些工作后，我有点担心自己可能会失败，于是我决定把电池插在笔记本电脑上，看看它是否能启动。我看到我的 BIOS 屏幕上挂着 Tux 和 Gnu 的图片，并做出了成功安装 libreboot 的执行决定。我安装了 Ubuntu 以确保一切正常，因为我已经有了一个 Ubuntu live-USB 记忆棒。甚至新的 WiFi 卡似乎也很好(除了它没有像英特尔卡那样的 5 GHz 天线，但这不是什么大问题)。

![Not an ideal place to get stuck. ](img/efd3667a2885c40d2d71c73e60b50067.png)

Not an ideal place to get stuck.

自由软件爱好者会注意到 Ubuntu 并不是自由软件运动的巅峰。它因包含专有软件、二进制 blobs 和其他问题而受到批评。也就是说，在最初的 Ubuntu 测试安装之后，我确实试图安装 Trisquel(在安装过程中崩溃，因为它混淆了 X200 没有光驱)、一个名为 Parabola 的 Arch 版本(无法从 u 盘启动)和另一个名为 gNewSense 的基于 Debian 的发行版(你不得不对这个可怕的名字发笑)，但我发现它们都很难安装，无法使用，或者两者兼而有之。

目前，我很高兴能够中和英特尔的老大哥，我可能会继续使用 Ubuntu，直到 libre 发行版有所改进(或者有一天我真的厌倦了，决定再试一次)。尽管安装 libreboot 的过程很繁琐，但这是可能的。我会向任何关心隐私、安全或自由的人推荐一台 libreboot 电脑。即使你不想把你的苹果扔进垃圾桶。
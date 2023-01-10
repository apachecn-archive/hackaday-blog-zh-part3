# 家庭自动化依赖于软件

> 原文：<https://hackaday.com/2016/08/02/home-automation-is-hung-up-on-software/>

家庭自动化是科幻小说中的最爱，从托尼·斯塔克(Tony Stark)的贾维斯(Jarvis)，到《杰森一家》(Jetsons)中的机器人女佣罗西(Rosie)，甚至是《星际迷航》(Star Trek)舞台工作人员拉的滑动门。事实上，大多数人都有一项最喜欢的技术，应该已经准备好在自己家里亮相了。那么这些东西在哪里？几周前我们[问过你](http://hackaday.com/2016/07/15/what-is-home-automation/)，压倒性的回答是软件还没有出现。

我们正在智能家居时代蹒跚而行，已经能够购买联网的车库门和恒温器有一段时间了。但是在大多数情况下，所有这些系统都是同一屋檐下的孤岛。自动化是 2016 年黑客日奖当前挑战[的主题。开发能把所有这些部分粘在一起的胶水将是一个很好的切入点。为什么那种胶水还不存在？](https://hackaday.io/prize/details#four)

我认为问题是双重的。一方面，没有一种明确的方法让许多设备在一个软件下工作。第二，当谈到家庭自动化时，真的没有一个很好的用户体验的明显例子。让我们看看为什么，并讨论什么将最终让我们到达那里。

## 人类接口

家庭自动化归结起来就是在房子里的人和控制房子的人机界面之间增加一个自动化层。这实际上是很难说服的。你的灯需要自动化吗？除了可靠的主电源之外，不需要任何东西，你就不能起床按下一个立即工作的灯开关，这难道不是懒惰吗？

这是一个棘手的问题。你的洗碗机是你懒惰的象征吗？毕竟，你仍然需要刮掉所有的残渣，装载到架子上，运行它，然后再次清空它。现在我想起来，进一步自动化洗碗机也将是一个很好的切入点。但我的观点是，在广泛采用之前，许多人肯定认为需要自动洗碗机是懒惰的，但现在他们非常渴望。为了让智能家居变得普及，我们需要让它的好处远大于转型的痛苦。

## 两个开关的故事

![WeMo WiFi light switch to the left of two "dumb" switches](img/eea0c852c14d1c040d7806c0c1452973.png)

WeMo WiFi light switch to the left of two “dumb” switches

我家里碰巧有两个比一般人聪明的电灯开关。一个是真正的物联网东西——一个 [WeMo 灯开关](http://www.belkin.com/us/F7C030-Belkin/p/P-F7C030/)——另一个是具有一些奇特功能的非连接开关。WeMo 控制我的门廊灯，我希望它在黄昏时打开，在晚上 11 点关闭。六年来，我一直使用一个带有可编程显示器的开关，随着天数和时间偏差的变化，设置和重置它是一件非常痛苦的事情。它终于死了(这是一个开关永远不应该做的)，我买了这个有 WiFi 的，但软件是可怕的，就像旧的开关一样痛苦。在股票设置不起作用后，我很庆幸能够通过切换到 IFTTT 来控制它，从而获得可靠的服务，此后再也没有碰过它。那次经历之后我不想了。

今年夏天早些时候，我在客厅升级了 LED 嵌入式照明。太亮了，我需要调暗一点。我知道这将是一个问题，所以我考虑选择一个眨眼枢纽和嵌入式灯和开关去了。我最后用了非无线电控制的(普通)灯和一个 Lutron Maestro 调光开关。这东西太牛逼了！您可以轻松设置灯光的最小和最大亮度，但您不必这样做。当你打开它的时候，使用双击来获得最大亮度，但是它仍然记得你的调光设置。长按关机键可以让你在关机前有大约一分钟的时间离开房间。

![Lutron Mestro dimmer is not dumb but not quite smart](img/80026e7c9437128e43068db3b0f769dc.png)

Lutron Mestro dimmer is not dumb but not quite smart

我认为 WeMo 交换机的硬件非常出色。但考虑到这两个开关，我喜欢 Lutron，对 WeMo 的看法很差，原因不外乎是糟糕的软件设置体验。这是家庭自动化问题的核心:用户无法将糟糕的软件体验与硬件分开，由于他们为硬件支付了高价，他们很可能会拒绝任何进一步的自动化冒险。

## 硬件锁定

硬件花钱而软件不花钱的观念是更大问题的一部分。硬件制造商有充分的动机来开发只与他们的硬件兼容的软件——如果你使用他们的免费应用程序/网站等，他们就赚不到钱。运行另一个制造商的硬件。这是一个很难解决的问题。

但它确实不止于此。假设硬件制造商允许第三方硬件在他们的系统上运行。如果第三方的东西工作不佳，可能会损害消费者对整个系统的看法。同样，这个问题没有明确的解决方案。

我想听听你对此的看法——袖珍手册的力量(我们购买和不购买哪些技术)是我们在这种情况下唯一的杠杆吗？我们可以做些什么来鼓励制造商不要将他们的硬件系统锁定在专有的生态系统中？

## 我们以前解决过这个问题

看看 PC 行业。您可以在戴尔、宏基、华硕或东芝笔记本电脑上运行相同的程序。你甚至可以改变你在这些机器上运行的操作系统，就此而言，软件公司可以让他们的产品在 MAC 上运行。这是因为有标准来定义这些计算机中的硬件，以便可以构建编译器，以及这些计算机如何与外界通信的标准(USB、以太网、WiFi 等)。).对于非计算机计算设备，如灯、电灯开关、冰箱、安全摄像头、门铃、机器人女佣等，我们需要这一点。

## 我们需要一个软件冠军

我们需要将硬件和软件分开，这样硬件公司就可以做他们最擅长的事情——制造年复一年可靠运行的经济实惠的设备。我认为在一个明确的软件冠军(或一群冠军)出现之前，这是不可能发生的。这意味着一个普通人可以理解、配置和直观操作的直观界面，就像你可以操作电灯开关一样。

这真是一个难题。你认为应该如何处理？有人构建这些软件工具的动机是什么？从下面开始对话。和上一期一样，我将挑选出一些最有趣的评论，并寄出 Hackaday t 恤衫。上次讨论后，我们给[aleksclark]、[DaveW]、[Dax]、[fountside]、[Ian Lee]、[j0z0r]、[jan]、[maxzillian]、[Neil Cherry]和[sangwiss]发了衬衫。

你喜欢 DIY 家庭自动化吗？现在是展示你的作品的好时机。立即加入您的项目，参加 [2016 Hackaday 奖](https://hackaday.io/prize/)的自动化挑战。20 名参赛者将每人赢得 1000 美元，并继续角逐 15 万美元的大奖。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)
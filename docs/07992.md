# 硬币电池驱动的海龟研究

> 原文：<https://hackaday.com/2017/12/15/coin-cell-powered-sea-turtle-research/>

黑客和修补总是有趣的游戏，但是当所有的努力都是为了做好事的时候，你必须要感激。[Nikos]通过将他对技术的兴趣与他对野生动物保护的热情结合起来，创造了一个低成本和超低功耗的温度记录仪——他正在为此使用一个[硬币电池](https://hackaday.com/2017/11/29/coin-cell-challenge-use-coin-cell-win-prizes/)，从而树立了一个榜样。

作为希腊一个海龟保护项目的创始人，[尼科斯]喜欢建造科学仪器来帮助他和他的团队完成任务。他的目标是在至少 180 天的时间内每 10 分钟记录一次温度，他设计了一个 PCB，大小刚好可以容纳一个 CR2032 硬币电池。其中 50 个最终将被密封在防水外壳中，并在整个研究期间埋在沙子里。

将设计限制在最基本的需求上，PCB 的其余部分包含一个数字温度传感器、一个保存这 180 天内所有记录的传感器值的 SPI EEPROM 和一个由 32.768kHz 晶体计时的 ATmega328PB。想知道如何处理 ATmega 的所有多余的、未使用的引脚，[Nikos]简单地将它们通过引脚头进行路由，从而将数据记录器转变为硬币电池供电的开发板。

假设您的记录间隔要求明显较低，您可能会很高兴听到[Nikos]估计理论上一个普通硬币电池可以为睡眠模式下的数据记录器供电 7 年以上，这使他有信心达到 180 天的目标。

Coin Cell ChallengeBuild something cool powered
by a coin cell, win prizes![Enter now](https://hackaday.io/contest/28283-coin-cell-challenge)[See all entries](https://hackaday.io/submissions/coin-cell-challenge/list)
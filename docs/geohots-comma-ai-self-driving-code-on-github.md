# GitHub 上 Geohot 的 Comma.ai 自动驾驶代码

> 原文：<https://hackaday.com/2016/12/01/geohots-comma-ai-self-driving-code-on-github/>

首先，[Geohot]有一个崇高的目标，那就是制造黑客版的自动驾驶汽车。然后是 comma.ai 和一大堆风险投资。在那之后，一封来自联邦政府的信和一次从商业领域的匆忙撤退。最新进展？ [comma.ai 的 openpilot 项目出现在 GitHub 上](https://github.com/commaai/openpilot)！

如果你有一辆讴歌 ILX 或者本田思域 2016 款旅行车，你可以开始自己使用这项技术。这是个好主意吗？你愿意在封闭的赛道上争取一些时间吗？

快速浏览代码可以得到一些关于这里发生了什么的线索。[电路板文件](https://github.com/commaai/openpilot/blob/master/board/main.c)显示了与这些汽车的驾驶控制接口是多么容易:有一堆 CAN 命令，仅此而已。有一些无意的黑色喜剧，像一个名为 [crash.py](https://github.com/commaai/openpilot/blob/master/common/crash.py) 的(软件)崩溃处理程序例程。

令人震惊的是，没有什么令人震惊的事情发生。这是一个非常简单的 Python，附带 c 语言。老实说，这看起来像是你可以很快上手的东西。有人想给我们发一辆讴歌 ILX 来测试吗？不保证你会完好无损地拿回来。

如果你错过了，请仔细阅读我们对 comma.ai 的[快速崛起](https://hackaday.com/2016/09/17/geohot-selling-his-self-driving-car-tech-for-1k-by-new-year/)和[更快撤退](http://hackaday.com/2016/10/29/geohots-self-driving-car-cancelled/)的报道。但我们认为游戏还没有结束:comma.ai 仍在招聘。开源自动驾驶汽车在我们的未来吗？那太棒了！

Via [Endagadget](https://www.engadget.com/2016/11/30/geohot-open-sources-semi-autonomous-technology/) 。感谢提示，[FaultyWarrior]！
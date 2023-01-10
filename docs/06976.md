# 开源 Barbot 只需要两个电机

> 原文：<https://hackaday.com/2017/08/31/open-source-barbot-needs-only-two-motors/>

大多数饮酒机器人都很复杂——有些是故意的，有些似乎是出于设计需要。如果你有一大堆酒，你仍然需要一种方法来以可控的方式把酒从瓶子里倒出来，通常是通过电动倾倒或泵送。有时候所有的管子、马达和电线看起来都很酷，很科幻。尽管如此，一个真正干净的设计并没有错。

[Lukas idlauskas 的] [开源 Barbot 项目](https://github.com/sidlauskaslukas/barbot)仅使用两个电机来驱动九个瓶子，仅使用一个 NEMA-17 步进器来沿着控制台的长度向下移动托盘，以及一个高扭矩伺服系统来触发 Beaumont Metrix SL spirit measures。当按钮被按下时，这些酒保的瓶子顶端分配 50 毫升，使它们(和重力一起)成为优雅地管理这么多瓶子的完美方式。饮料选择在一个应用程序上进行，通过蓝牙连接到运行节目的 Arduino Mega。

Barbot 是一个开源项目，项目文件可以从[Lukas]的 GitHub 知识库
中获得，讨论在[Slack group](https://openbarbot.herokuapp.com/)中进行。

如果你想要的是 barbot，看看这个[增效器 4-饮料 barbot](https://hackaday.com/2014/05/25/synergizer-the-emergency-key-turn-barbot/) 和我们不久前发表的[联网 barbot](https://hackaday.com/2013/12/31/barbot-mixes-drinks-perfectly-with-web-interface/) 。

 [https://www.youtube.com/embed/1JVnOlu0Daw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1JVnOlu0Daw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 

[通过[使](http://makezine.com/2017/08/29/edible-innovations-meet-barbot-open-source-cocktail-mixer/)
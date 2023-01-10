# 被黑的公寓对讲机会对你吠叫或让你进来

> 原文：<https://hackaday.com/2015/10/08/hacked-apartment-intercom-barks-at-you-or-buzzes-in/>

忘了你的公寓钥匙？如果你有一栋有门卫的豪华建筑，没问题。如果你的住所稍微简朴一点，你可能只有一个内部通话面板，可以呼叫你的公寓，这样有人就可以按门铃让你进去。但是如果没人在家，你就不走运了。这就是为什么[pawez]花了一个小时快速制作了一个装满好东西的[对讲机连接的自动化系统](http://silent.org.pl/home/2015/10/04/entry-phone-hack/)包。

设计非常简单——一个 ATMega328P 可以在按下内部通话按钮时监听公寓里的模拟电话铃声，一个与门开关并联的继电器可以让他进来。为了增加安全性，微控制器检测按钮按压的模式，并防止不受欢迎的客人进入大厅。当[pawez]添加了一个 PCM 音频模块来通过对讲机播放随机音频剪辑时，事情变得非常有趣。正如你在下面的视频中看到的，不正确的代码可能会导致狗叫或口头奚落。但[pawez]因收录了《超级马里奥兄弟》的声音片段以及将《帝国进行曲》与《伊帕内玛的女孩》混搭在一起而获得了额外的加分。

没错，我们之前已经看过这个项目的[版本，比](http://hackaday.com/2012/04/09/apartment-entry-morse-code-lock/)稍微精致一点，但不像【马里奥】版本，但是这个特别的黑客的展示让我们笑得合不拢嘴。

 [https://www.youtube.com/embed/e9GWteVUYD0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e9GWteVUYD0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[谢谢，哈克索]
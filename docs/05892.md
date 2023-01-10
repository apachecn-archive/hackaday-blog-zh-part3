# 老式便携式电视变成复古游戏系统

> 原文：<https://hackaday.com/2017/05/11/vintage-portable-tv-turned-retro-gaming-system/>

当[FinnAndersen]在路边发现一台旧电视机时，他做了任何自尊的 DIY/游戏爱好者都会做的事情:他把它拆开，并在里面安装了一台运行 RetroPie 的 Raspberry Pi 3，以便在复古电视上玩复古游戏！

[芬恩]在意识到 CRT 真的能工作之前，把它从电视里拿出来。已经太晚了，所以[芬恩]订购了一个 12 英寸的液晶显示屏来代替它。不过，他喜欢 CRT 的弯曲屏幕的想法，所以他在 CRT 周围模制了一块丙烯酸树脂，经过一些切割和研磨，使其适合屏幕的空间。

[芬恩]也喜欢电视仍然能够观看电视信号的想法，所以他买了一张电视调谐卡。经过几次改装后，他可以用电视原来的频道转换器来控制这张卡。他使用 Arduino 来读取原始电视使用的旋转编码器的状态。经过一些尝试和错误后，[Finn]能够读取频道位置，Arduino 会向调谐器卡上的频道上下按钮发送信号，以便更换频道。

接下来是音频。[芬恩]找到了一个比电视更好的扬声器，所以他调换了它们，并增加了一个放大器。还是用原来的音量旋钮来控制音量。USB 集线器隐藏在电视底部的侧面，允许控制器连接，最后，电源将电源电压转换为 12V DC，运行树莓 Pi 和电视调谐器。

[FinnAndersen]利用一台外观精美的老式电视建造了一个非常棒的复古橱柜。不幸的是，他在弄清楚他可以使用 CRT 之前就把它拆下来了，但是新的看起来相当不错！额外的优势是什么？算是便携的吧。至少，没有了里面的 CRT，它比以前轻多了。[这里](http://hackaday.com/2015/12/09/retro-tv-breathes-new-life-with-a-raspberry-pi/)是一台旧电视里的另一个复古控制台，[这篇文章](http://hackaday.com/2016/10/21/send-a-raspberry-pi-back-in-time-to-1980/)是关于将树莓皮连接到你能得到的每一个显示器上。

 [https://www.youtube.com/embed/hu4SaxqlHVo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hu4SaxqlHVo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


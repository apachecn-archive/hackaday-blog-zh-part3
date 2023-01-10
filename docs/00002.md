# 这是一架立式钢琴，这是一个活套，这是一个圆周率项目

> 原文：<https://hackaday.com/2015/09/06/its-an-upright-piano-its-a-looper-its-a-pi-project/>

我们真的不怎么出门，但我们注意到这些天在公共场所有色彩鲜艳的立式钢琴。研究表明，这些钢琴是由小型、独立的当地组织放置的，其中大多数旨在传播音乐的快乐，鼓励社区意识。

[Sean 和 Mike]用他们的模拟循环钢琴 [Quaver](http://blog.majormega.com/looping-piano) 进一步发展了这个想法。他们都是宾夕法尼亚州兰开斯特的制造商/音乐家，而兰开斯特恰好是公共钢琴的热点城市[。[Sean 和 Mike]经常停下来弹奏它们，并希望找到一种好方法来捕捉它们的即兴杰作。八分音符是](http://musicforeveryone.net/)[一个古董竖琴，经过改装](https://imgur.com/a/9HY0q)可以录制、保存、循环和上传音乐到互联网。它通过一个简单直观的用户界面和一个 Raspi 2 完成所有这些工作。八分音符的工作方式很像一个 4 声道录音机，所以最多四个人可以创作一首歌曲。

玩家坐下来，打开指关节，按下我们个人最喜欢的界面部分:巨大的、不可抗拒的录音按钮。一个友好的滚动 LED 矩阵显示器告诉他们开始播放。一旦他们感到满意，他们再次按下按钮停止录音，他们演奏的音符立即通过一对从 20 世纪 80 年代回收的 Bose 扬声器循环播放。这只是有趣的开始，随着你的循环录音一起演奏，建立起几个值得歌唱的声部！

Quaver 的发展并非没有问题。钢琴在任何环境下都很难拾音，尤其是普通购物中心的美食广场。因为钢琴的共鸣板非常大，所以声音不会集中在任何一个地方。一位名叫[Ezra Charles help impilla]的电子工程师在 20 世纪 70 年代早期创造了电磁条形拾音器，并以自己的名字命名。它们很快成为像埃尔顿·约翰这样的钢琴明星的首选扩音设备。用磁铁和夹子将拾音器固定在钢琴音板上。它们只感知振动，所以不需要担心反馈。

放大并不是他们遇到的唯一问题。当用户重置钢琴时，Pi 会重新启动。在标准的 Raspbian 中，这可能需要 30 秒，这在公共环境中效果不好。人们会很快失去兴趣并走开。[Mike]最终使用 [Buildroot](http://buildroot.uclibc.org/) 编译了他自己的 Linux 内核，并且能够将启动时间降低到令人钦佩的 2.9 秒。

查看八分音符视频演示，然后去听人们上传的循环。

 [https://www.youtube.com/embed/JJ90NiB1rw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JJ90NiB1rw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


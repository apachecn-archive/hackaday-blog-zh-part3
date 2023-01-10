# 令人毛骨悚然的说话神经网络

> 原文：<https://hackaday.com/2017/03/22/creepy-speaking-neural-networks/>

技术艺术家[Alexander Reben]与我们分享了一些正在进行的工作。是在各种名人言论 (YouTube，下面嵌入)上训练出来的[神经网络。[亚历山大]的艺术目标是捕捉一个人声音的“灵魂”，就像几个世纪前的](https://www.youtube.com/watch?v=CWLqlXCu3OM)[死亡面具](https://en.wikipedia.org/wiki/Death_mask)一样。当然，听[Alexander]的《Rob Boss》并不能代替实际观看一盘旧的鲍勃·罗斯磁带——事实上，它甚至从来没有说出“快乐的小树”——但它肯定是这个人自己，现在我们可以产生无限量的他的口头禅。

在幕后，他正在使用 WaveNet 来训练网络。基本上，该算法将音频流分割成块，并试图根据前一状态预测下一个块。训练音频数据的一些预编辑是必要的——例如，从科尔伯特音轨中移除笑声和掌声——但它基本上只是被插入。

网络似乎过分强调西伯利亚人；在现实生活中，我们从未听过巴拉克·奥巴马发出这样的嘘声。将噪声输入到被设置为模式识别器的机器中，往往会将它们推向极限。但是为了与这一系列项目的名称“算法的不合理人性”保持一致，它做得相当好。

他还对多名演讲者做了同样的事情(也是 YouTube)，在这种情况下，有 110 名不同性别和口音的人。人与人之间的差异会产生更平滑、更人性化的声音，但显然也不是针对某个人。它意味着从雕塑口中的扬声器里持续不断地流出。我们有点害怕，还好。

我们以前报道过一些[亚历山大]的作品，从令人畏缩的"[机器人咬人](http://hackaday.com/2016/06/15/robot-bites-man/)"到知性概念的"["所有现有艺术](http://hackaday.com/2016/04/21/all-prior-art/)"。继续加油，[亚历山大]！

 [https://www.youtube.com/embed/CWLqlXCu3OM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CWLqlXCu3OM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


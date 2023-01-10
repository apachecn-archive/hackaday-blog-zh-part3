# 火花隙和内聚器遇到比格犬骨

> 原文：<https://hackaday.com/2016/03/29/spark-gap-and-coherer-meet-beagle-bone/>

回归基础是自学一项技术的好方法。我们经常在用与非门甚至分立晶体管构建的计算机中看到这种情况。收音机也是一样——把它剥离到 19 世纪真的可以让你拥有这项技术。但是，如果一个老派的无线设置仍然需要一个 21 世纪的转折来点燃你的火，[尝试这个火花隙发射机和相干接收机与比格犬骨莫尔斯解码器](http://ashishrd.blogspot.com/2016/03/19th-century-radio-technology-meets_20.html)。

从本质上来说，火花隙发射器只是一个宽带射频噪声发生器，因此目前操作这种发射器是相当非法的。Ashish Derhgawen 的版本没有 LC 调谐电路，如果它有天线，将会特别令人讨厌。但即使没有一个，100%机电发射器对几英尺来说也是好的——在不引起当地火腿愤怒的情况下进行实验绰绰有余。

接收器是基于相干器，一种只有当经过的无线电波干扰它时才导电的装置。[Ashish]的内聚器是一个塑料管中两个螺栓之间的铁屑块。为了重置凝聚器，[Ashish]增加了一个由电磁门铃环制成的去凝聚器，用来敲击管子，将锉屑推回到非导电状态。他还添加了一个光隔离器来调节 Beagle 上 IO 引脚的接收器输出，并添加了一个 Python 脚本来解码输入的莫尔斯信号。你可以在下面的视频中看到它的运行。

如果这个版本看起来很熟悉，那是因为[我们在](http://hackaday.com/2015/11/22/the-first-radio-sets-a-spark-gap-and-a-coherer)之前已经介绍过了【Ashish】的成果。但这个项目一直在发展，很高兴看到他把它带到了哪里，学到了什么——比如 MOSFETs 不太喜欢电感反冲。

 [https://www.youtube.com/embed/eL-ndyN-mGU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eL-ndyN-mGU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


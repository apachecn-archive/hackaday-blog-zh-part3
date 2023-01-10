# 这个 WAV 文件可能会混淆你的 Fitbit

> 原文：<https://hackaday.com/2017/03/15/this-wav-file-can-confuse-your-fitbit/>

随着我们周围的设备与世界其他地方的联系越来越紧密，人们越来越关注它们在互联网方面的安全性。重要的是要记住，虽然这不是唯一可能的攻击媒介，通过他们可以妥协。所有集成了传感器或指示器的设备都有可能以某种方式被利用，无论是简单的嗅探通过闪烁的 LED 表示的数据流，还是更复杂的攻击。

密歇根大学和南卡罗来纳大学的研究人员展示了针对 MEMS 加速度计的成功攻击，比如你可能在智能手机中找到的 MEMS 加速度计。他们使用精心制作的声波，可以随意复制该设备应该能够返回的任何输出。

MEMS 加速度计具有微小的簧上重量，突出的板形成一组电容器的一部分。加速度引起的重量位移是通过观察两块板两侧电容之间的差异来测量的。

该团队在我们放在休息时间下方的视频中描述了他们的工作，尽管令人沮丧的是，除了提到反走样之外，他们没有谈到足够多的细节。我们怀疑他们振动重物，使其与传感器的采样频率相匹配，并不断记录其行程中某一点的读数，他们可以通过施加声音的相位来拨号。他们演示了对智能手机控制的模型车的干扰，以及在 Fitbit 中添加的虚假步骤。整个事情足以让《纽约时报》担心用声波窃听电话，这是一种可以预见的过度反应，但研究人员自己并不认同。

 [https://www.youtube.com/embed/Dfc3jZkcnLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Dfc3jZkcnLU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前已经解释过【MEMS 加速度计如何工作，以及了解过[气隙利用](http://hackaday.com/2017/02/02/hacking-the-aether/)。在这一点上，没有必要太担心你的设备，但要记住这是一种有趣的替代输入方法。

谢谢[Sterna]的提示。
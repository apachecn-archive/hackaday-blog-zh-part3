# 通过计算圆周率获得雨天乐趣

> 原文：<https://hackaday.com/2016/08/24/rainy-day-fun-by-calculating-pi/>

如果你需要一个真正随机的事件发生器，那就等着下一场暴雨吧。地面上的任何给定点是否在特定时间被水滴击中都是任何人的猜测，这种随机性是这个简单装置的关键，它使用雨滴传感器估计圆周率的值。

你可能还记得[AlphaPhoenix]最近的《卡坦远征者的电击定居者》。这个不太令人震惊的构建的想法是使用方形传感器与圆形传感器的面积比来估计圆周率的值。简单的压电传感器充当冲击传感器，为 Arduino 提供信息，并计算击中传感器的雨滴的相对数量。在下面的第一个视频中，我们看到随着更多数据的积累，Arduino 对 pi 的估计最终收敛于众所周知的 3.14159 值。第二个视频详细介绍了该方法背后的数学原理，并讨论了测试过程中出现的现实问题——事实证明，防水和接地都是传感器垫无噪声数据的关键。

最后，[AlphaPhoenix]没有证明任何新的东西，但是我们喜欢这里的方法，并且可以看到它的应用。使用这种传感器来检测单个爆米花粒的爆裂来演示高斯分布怎么样？我们也会情不自禁地想到其他测量雨滴的方法；当雨水在方形和圆形容器中有差别地累积时，用应变仪来称重怎么样？请在下面的评论中分享你的想法。

 [https://www.youtube.com/embed/I-BC_vI4CAE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I-BC_vI4CAE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/akmFVxh1ZPQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/akmFVxh1ZPQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[遥控/电子](http://reddit.com/r/electronics/comments/4z6lup/i_built_a_circuit_that_calculates_pi_with_a/)
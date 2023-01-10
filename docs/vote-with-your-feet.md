# 用脚投票(用去或不去某处表示想法)

> 原文：<https://hackaday.com/2016/11/12/vote-with-your-feet/>

游戏化的生活是愚蠢的，有趣的，也是和你每天遇到的陌生人互动的好方法。这里有一个例子，可能会在你下一次去上班的路上突然出现。这是一种对任何话题进行非常不科学的投票的方式——你甚至不用用手投票。

一个名为[用脚投票]的组织想出了一种新颖的投票方式。简单地走在人行道上，穿过两个门口中的一个，每个门口都标有二分法的两边。每个门口都能够统计通过的人数，因此任何可以想象的问题都可以被调查。他们已经做了 [vim vs emacs](http://hackaday.com/2016/07/26/editor-wars/) (59 比 27)，我们希望看到 [Keynes vs Hayek](https://www.youtube.com/watch?v=d0nERTFo-Sk) ，甚至阿华田 vs Nesquik。用户可以向机器发送新的问题供大众投票，因此娱乐活动完全是由你的想象力来决定的。

物理构造[被很好地记录下来](http://www.instructables.com/id/Vote-With-Your-Feet/)。由于这是在户外使用的，选择[一个 flipdot 显示器](http://www.instructables.com/id/Howto-Flipdot-With-a-Raspi/)(当然玩起来总是很有趣)对于任何光线水平下的高对比度都是完美的。每个门口都有[一个光束传感器](https://www.automationdirect.com/adc/Shopping/Catalog/Sensors_-z-_Encoders/Photoelectric_Sensors/18mm_Cube_-_NonMetal/Polarized_Retroreflective_(GX_Series)/GXP-AN-1E)，由树莓 Pi 驱动头顶的显示器进行监控(如果你想深入了解，这里有全部的[代码)。](https://github.com/vwyf)

像这样的艺术装置的重点是让人们以一种新颖的方式与他们的环境互动，这个项目已经完成得非常好了。三天之内，他们注册了超过 10，000 张选票，这些选票可以在他们的网站上看到。如果你有一个需要数据可视化的项目，你可能想把它放在你的口袋里。

如果你自己也在寻找灵感的话，我们还看到了门道统计投票之外的人数的其他方法。
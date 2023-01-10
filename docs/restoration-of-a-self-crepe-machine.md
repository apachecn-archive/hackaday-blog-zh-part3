# 自绉机的修复

> 原文：<https://hackaday.com/2016/03/18/restoration-of-a-self-crepe-machine/>

几年前,[ Tweepy ], hack aday 读者群的全球煎饼爱好者之一，拥有了一台老旧的“自制薄饼”机。从 20 世纪 80 年代初集成电路上的日期代码来看，这台机器在大约 30 年的时间里，在插入 1 法郎硬币(当时约为 17 美分)的情况下，烹饪并出售一个新鲜的皱皮。

可悲的是，它不再生产焦糖布丁了。老化的控制逻辑是罪魁祸首，而不是调试它[【Tweepy】决定用一个微控制器](http://www.skling.fr/2008/12/16/restauration-self-crepes/)(法语，[谷歌翻译链接](http://translate.google.com/translate?sl=auto&tl=en&u=http%3A%2F%2Fwww.skling.fr%2F2008%2F12%2F16%2Frestauration-self-crepes%2F))取代它。他选的那个(标着“RSF2127”，有人能认出来吗？)采用 QFP 封装，因此将它连接到 0.1 英寸的原型板上需要用细导线进行焊接，但它很快就可以运行了。一些轨道切割和布线到原来的 PCB，定制的 C 代码已经准备好了。

该机器制作皱皮的部分采用了一个加热辊，与我们最近推出的[南非环形煎饼机器](http://hackaday.com/2016/03/11/endless-pancakes/)中的加热辊没有什么不同，在评论帖[Tweepy]中提到了这一点，但似乎只使用了单面烹饪工艺。滚筒有一个圆形绉丝大小的凸起区域。为了开始烹饪过程，面糊的装载槽被带到滚筒下面，然后滚筒旋转，使得圆形凸起区域穿过面糊的表面。当滚筒转动时，它会烹饪皱皮饼，然后将皱皮饼从滚筒转移到输出槽。整个过程依赖于一个预制面糊库，遗憾的是它不是一个奶油蛋糕复制器。另一方面，制作一个蛋糕大约需要 40 秒钟，只要你在机器里放上面糊，它就可以连续生产。

我们喜欢蛋糕，我们喜欢机器，我们喜欢[Tweepy]用它做的东西。如果这些机器中的任何一个越过了法国的边界，我们在英语世界的角落里也从未见过。这是一个耻辱，因为谁不想在他们的黑客空间里的水壶和微波炉旁边放一个呢！不过，他们需要为英语市场改进这个名字。

我们最近在 Hackaday 上对与煎饼相关的黑客进行了总结，因此没有必要重复。然而，这并不是我们看到的第一次自动售货机被黑。有这个[秘密升级的汽水贩卖机](http://hackaday.com/2010/05/17/old-school-vending-machine-learns-new-tricks/)，这个[发微博的啤酒贩卖机](http://hackaday.com/2011/11/25/beer-dispenser-talks-to-customers-announces-office-parties-via-twitter/)，或者这个[开源软件机器怎么样，它肯定没有出售](http://hackaday.com/2012/03/06/freedom-toaster-dispenses-foss-for-free/)。
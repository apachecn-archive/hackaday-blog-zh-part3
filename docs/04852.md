# 弗兰肯夸德飞起来了

> 原文：<https://hackaday.com/2017/01/25/frankenquad-takes-to-the-air/>

现代四轴飞行器的飞行控制器在平衡俯仰、偏航、倾斜和油门之间跳着微妙的舞蹈。得益于现代 MEMS 陀螺仪和加速度计，他们可以做到这一点。当马达、螺旋桨和速度控制器相对匹配时，这项工作很容易。但如果他们不是呢？这就是[skitzopvv]通过构建 Frankenquad 来回答[的问题。Frankenquad 是一个 250 大小的 FPV 四轴飞行器，有 4 个不同的马达和 4 个不同的螺旋桨。不同制造商的道具大小不同，甚至包括 3 个和 4 个刀片单元的组合。如果这还不够,[ skitzopvv]使用了 3 种不同的电子速度控制器。每个速度控制器都有一个运行不同固件的微处理器，这意味着它对油门输入的响应略有不同。](https://www.youtube.com/watch?v=-sXnhjgPsC4)

控制这一切的是[skitzopvv]品牌版本的赛车反抗 R4 飞行控制器。rebel 由 STM32F4 系列 ARM 微控制器供电。这些控制器中的大多数运行的是 cleanflight 开源飞行控制软件的变体。问题是——它能处理 4 种不同动力组合的不平衡推力和扭矩吗？

飞行测试证明答案是响亮的是。四轴飞行器很容易盘旋。正如视频显示的那样，[skitzopv]继续用它在天空中烧了几个洞。无可否认，[skitzopfv]是一个比我们任何人都好得多的飞行员。他确实注意到了一点小偏差和朝向较小螺旋桨的明显偏航。尽管如此，令人惊讶的是，一个现代飞行控制器竟然能够轻而易举地将一堆垃圾部件变成一架飞行的四轴飞行器。你可以在这里了解更多关于飞行控制器的信息。

 [https://www.youtube.com/embed/-sXnhjgPsC4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-sXnhjgPsC4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


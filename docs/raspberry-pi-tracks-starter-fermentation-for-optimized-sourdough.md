# 树莓 Pi 跟踪发酵剂发酵，优化酸面团

> 原文：<https://hackaday.com/2018/06/27/raspberry-pi-tracks-starter-fermentation-for-optimized-sourdough/>

没有吃过真正的酸面团的人也没有吃过真正的面包。美食在你吃的时候会有一点反击，一个合适的酸面团，有着松脆的外皮和扑鼻的中心，当然符合要求。酸味面团的爱好者，包括你的卑微的作家，都有我们假装是古老的家庭秘密的食谱，而事实上我们都只是猜测。酸面团部分是科学，部分是艺术，但主要是美味的黑魔法。

为了揭开他的酸面团制作过程的神秘面纱，[Justin Lam]用这个图像处理酸面团发酵监视器进行了数字化处理。酸面团面包不是通过添加啤酒酵母(*酿酒酵母*)来发酵的，而是通过加入一种发酵剂来发酵的，这是一种由野生酵母组成的充满活力的生态系统，经过精心培育，有时长达数年。像任何其他生物一样，它需要被喂养，这个任务应该发生在最大发酵的时候。[Justin]没有猜测这可能是什么时候，而是用 Raspberry Pi Zero 和 PiCam 捕捉了一段开胃菜的延时视频，因为里面的小动物发出了它们的 CO₂，因此在它的容器里展开了它。一个小 Python 做了阈值处理的工作，并在启动器上升时找到它的顶部，允许[Justin]绘制启动器随时间变化的高度。他发现高峰高度，因此发酵高峰，发生在喂食后大约六小时。他已经利用他的数据更好地通知他的喂养计划，并学习如何最好地恢复被忽视的首发。

令人惊讶的是，这不是我们第一次在这里讨论酸面团。似乎有人使用 [Git 进行迭代的酸面团配方开发](https://hackaday.com/2018/05/09/breadboarding-git-for-a-b-testing-actual-bread/)，我们曾经介绍过[一家由热解的酸面团](https://hackaday.com/2017/07/21/the-tuna-fish-sandwich-foundry/)制成的铸造厂。

[https://videopress.com/embed/1jrRbYB2?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0](https://videopress.com/embed/1jrRbYB2?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0)
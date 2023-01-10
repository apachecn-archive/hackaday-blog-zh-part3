# 钢铁侠面具带 HUD！

> 原文：<https://hackaday.com/2018/03/25/iron-man-mask-with-a-hud/>

在某些时候，孩子不可避免地会梦想成为超级英雄。不是所有的孩子都有机会看到梦想的实现，但是有一些孩子把命运掌握在自己手中。Redditor [Lord_of_Bone]抓住这个目标，为自己打造了一个集成 HUD 的钢铁侠面具[！](https://314reactor.com/2018/03/18/pi-ron-man/)

依靠他以前建立的一个概念上类似的项目，许多代码被重新散列为这个“马克 2 号”版本。智能手机全息金字塔的碎片充当投影表面——使用镜头聚焦图像，以便在如此近距离观看——以及一对显示信息的有机发光二极管屏幕。令人高兴的是，背光的缺失导致用户视野中只显示文本。

[骨之王]没有用 J.A.R.V.I.S .说话，而是用一个树莓 Pi Zero W 作为面具的大脑。解决有机发光二极管屏幕和 Enviro pHat 之间的一些 I2C 问题需要一个快速的 veroboard 和一些硬件黑客。将所有东西塞进面罩并不是一件容易的事情——使用 Blutack 和 Sugru 将它们束缚在有限的空间内——但是 pHat 必须在户外表面安装，以获得大气和光线数据。

 [https://www.youtube.com/embed/dCUxfEzlKXU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dCUxfEzlKXU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



现在，该遮罩显示 RGB 光线值和亮度、温度、压力、x-y-z 速度以及北向度数。未来的计划包括增加一个更亮的有机发光二极管，因为高亮度会破坏显示器，以及更多的数据类型——比如 WiFi 信息，或者他的组合[测距仪和弹药计数器](https://hackaday.com/2017/09/02/nerf-gun-ammo-counter-and-range-finder/)。

[Via[/r/RASPBERRY _ PI _ PROJECTS](https://www.reddit.com/r/RASPBERRY_PI_PROJECTS/comments/85ed0l/piron_man_wearable_iron_man_mask_with_hud/)
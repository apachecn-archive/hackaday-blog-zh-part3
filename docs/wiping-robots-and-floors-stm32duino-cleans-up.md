# 擦拭机器人和地板:STM32duino 清理

> 原文：<https://hackaday.com/2018/06/21/wiping-robots-and-floors-stm32duino-cleans-up/>

有没有发现自己身边躺着 19 个不知名的机器人吸尘器？没有吗？嗯，[亚伦克里斯托菲尔]喜欢过着[不同的生活，充满了斑马纹机器人](https://atcnetz.blogspot.com/2018/06/custom-firmware-fur-staubsauger-roboter.html) ( [翻译](https://translate.google.com/translate?hl=en&sl=de&tl=en&u=https%3A%2F%2Fatcnetz.blogspot.com%2F2018%2F06%2Fcustom-firmware-fur-staubsauger-roboter.html))。拆了几个后，只剩下十个真空吸尘器——伤亡是预料中的事。通过他们的牺牲，他发现一个 STM32F101VBT6 处理器充当幸存者的大脑。巧合的是，有一个名为 [STM32duino](https://github.com/stm32duino/wiki/wiki) 的项目旨在让那些处理器与我们喜欢或讨厌的 Arduino IDE 一起工作。【Aaron Christophel】通过项目快速添加了一个变体板，扣下了。

当然，他只需利用机器人顶部液晶显示屏的背光，启动并运行。从那里，STM32 处理器给了他整整 80 个 GPIO 引脚来玩。经过大量的修补，他控制了所有的传感器、马达和灯光。考虑到他们每个人都有一个遥控器，几个红外线传感器和轮子，[Aaron Christophel]现在有一个小型机器人舰队随时待命。他的工作间现在一定很干净了。也许他下一步会给吸尘器增加一个互相交流的方式。一个机器人完成工作，但整个团队完成工作的风格，特别是与斑马纹清洁器在最前线。

如果你想看更多他的作品，他的网站上有相当多的视频展示了这个项目的前前后后——一定要带一个翻译。他甚至为那些想要复制他作品的人准备了一个方便的图钉。如果你想直接进入 STM32 编程，我们有一篇关于如何安装和调试 STM 32 的文章。否则，请欣赏[Aaron Christophel]对八个红外距离传感器和运行它们的定制固件的演示。

 [https://www.youtube.com/embed/zwJjFtI88kE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zwJjFtI88kE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


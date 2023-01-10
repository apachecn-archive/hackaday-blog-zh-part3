# 12 英尺吉他登台

> 原文：<https://hackaday.com/2017/06/24/12-foot-guitar-takes-the-stage/>

音乐节既有趣又令人兴奋。它们是人们表演和展示艺术的机会。今年 6 月在堪萨斯城举行的 Boulevardia 活动就是这样一个活动，其中一个互动展品是一把可以演奏的 [12 英尺长的吉他](https://medium.com/@riebschlager/creating-a-playable-12-foot-tall-electric-guitar-f949ccc786d6)。[Chris Riebschlager]分享了他制作该乐器的经验，该乐器旨在欢迎活动中的游客。

这个美丽装置的核心是一块裸露的导电板，用来检测琴弦上的触摸。该信息通过串行通信发送到 Raspberry Pi，然后 Raspberry Pi 选择相应的 WAV 文件进行播放。额外的 arcade 按钮允许从 A 到 G 选择可演奏的和弦，包括大调和小调，还可以选择将吉他置于干净或脏模式。

建筑的简单令人惊叹。电容式触摸板使用 Arduino IDE 编程，代码作为[要点](https://gist.github.com/riebschlager/01b96e8856499a8605d3fe864e315e60)提供。Raspberry Pi 运行一个 [Python 脚本](https://gist.github.com/riebschlager/4d329324f6520e41a9994d8b5696f460)，使系统表现得像一把真正的吉他，即触摸并按住琴弦使其静音，同时松开琴弦产生相关的声音。为了更好的一致性，正在播放的音符是从车库乐队导出的吉他音符。

物理结构由中密度纤维板和钢组成，吉他的琴身和琴颈由数控机床加工而成。油漆，整理和自定义贴花给完成的项目一个摇摆的外观。查看以下制作过程的视频以及完成设计的照片[。](https://medium.com/@riebschlager/creating-a-playable-12-foot-tall-electric-guitar-f949ccc786d6)

这个项目是技术支持艺术的一个很好的例子，如果你喜欢吉他，那就去看看布莱恩·梅的手工吉他。

 [https://www.youtube.com/embed/iElgK3UEwE4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iElgK3UEwE4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/C5Yxru3rIM8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C5Yxru3rIM8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/xAMeLUiwPnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xAMeLUiwPnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 读卡器锁定可阻止未经授权的工具用户

> 原文：<https://hackaday.com/2018/05/20/card-reader-lockout-keeps-unauthorized-tool-users-at-bay/>

这是每个黑客空间、大学机械商店、甚至有严重控制问题的父母的家庭商店都有的问题:你如何确保只有受过训练的人员在操作机器？有各种各样的方法来解决这个问题，但是为什么不扔一点科技在它上面，比如这个磁卡读卡机锁定？

[OnyxEpoch]没有透露他属于上述哪一类，如果有的话，但我们会大胆猜测这是一个黑客空间，因为它在这样的环境下会工作得很好。内置于坚固的钢外壳中，内部结构非常简单——一个带 USB 屏蔽的 Arduino Uno、一个 SD 卡和一个数据记录器，以及一个 LCD 显示屏和各种按钮和开关。这个东西的核心是一个 USB 磁卡读卡器，安装在外壳的前面。

要解锁机器，用户刷一下他或她的卡，如果管理员之前已经将他们添加到列表中，继电器就会给工具加电。当然，有一个用于本地覆盖的按键开关，以及一个用于在使用点编程的管理模式。工具的使用是按日期、时间和使用者来记录的，这使得识别捣乱者和其他违法者变得容易。

我们发现它令人印象深刻地完整，但是想象一下在机器操作过程中出现会话超时至少是令人讨厌的，甚至是潜在的危险。也许解决办法是在超时临近时发出一个非常明显的警报— [一个樱桃色的陀螺就可以了](https://hackaday.com/2016/11/19/jenkins-and-slack-report-build-failure-light-the-beacons/)！

如果你是一个为黑客空间寻找好点子的人，有更多的阅读材料。我们之前已经讨论过黑客空间安全的基础知识，以及黑客空间的 T2 保险。

 [https://www.youtube.com/embed/M08HMr_rnAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M08HMr_rnAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


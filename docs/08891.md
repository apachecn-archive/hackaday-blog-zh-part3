# RFID 解锁你的电脑，因为你是 1337

> 原文：<https://hackaday.com/2018/03/17/rfid-unlock-your-pc-because-youre-1337/>

有没有想过成为 90 年代末电影黑客中的一员？是的，你的地下室充满了超频的 Linux 设备，你已经确保所有的终端窗口都设置为黑底绿字，但这并不总是足够的。[你需要的是一个 RFID 标签，当你用你的 RFID 卡触摸阅读器时，它会解锁你的电脑](http://ls-homeprojects.co.uk/project-guide-rfid-login/)。*只有到那时*你才可能继续在你众多的键盘上狂轰滥炸，勇敢地尝试*黑掉主机。*

[Luke]为我们带来了这个版本，想要一种更简单的方法来快速登录，而不牺牲基本的安全性。由于 RC522 RFID 阅读器已经在手边，这成为了该项目的基础。这款阅读器与 Sparkfun Pro Micro Arduino 克隆产品捆绑在一起，两款设备都意外地运行在 3.3V 上，无需任何电平转换器。代码很简单，基于现有的 [Arduino RC522 库。](https://github.com/miguelbalboa/rfid)成功扫描到正确的标签后，Arduino 充当 HID 键盘，将用户密码和回车一起输入电脑，解锁机器。简单！

总的来说，这是一个整洁的构建，实现了[卢克]设定的目标。这是一种只需几个零件和一天的工作就可以复制的东西。如果你对底层细节感兴趣，我们之前讨论过将 Arduinos 转变为 USB 键盘。
# 游戏卡中的雅达利 2600

> 原文：<https://hackaday.com/2017/07/08/atari-2600-in-a-game-cartridge/>

[PJ 埃文斯]有一个毁了的游戏卡带躺在那里，只是等待一个项目。作为 Activision 为 Atari 2600 游戏机开发的 F-14 Tomcat 游戏，它似乎已经成熟，可以用作某种项目外壳。当他遇到几个 9 针 D-sub 操纵杆端口时，他有了一个想法。他意识到他的 Rasperry Pi Zero 可以装进弹药筒。添加一个电源按钮，电视颜色选择器，难度开关，以及选择和重置按钮，你就有了一个模拟器。

[PJ]的 Pi Zero 有足够多的 GPIO 引脚来容纳所有这些按钮和开关，再加上一堆操纵杆。为什么不把模拟器放在游戏盒里呢？在软件方面,[PJ]研究了 Adafruit 的[复古游戏和树莓派](https://learn.adafruit.com/retro-gaming-with-raspberry-pi/)资源，其中有大量关于设置游戏模拟器的建议。他决定让 [RetroPie](https://retropie.org.uk/) 操作系统帮他找出所有的引脚，让 [Stella](https://stella-emu.github.io/) 做实际的雅达利 2600 仿真。

谢谢， [@seb_ly](https://twitter.com/seb_ly/status/881145540922277888) ！
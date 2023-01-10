# 圣诞玩具既不是球形的，也不运行 Arduino

> 原文：<https://hackaday.com/2015/12/26/christmas-bauble-is-neither-spherical-nor-runs-arduino/>

[Jordan Wills]被他的公司 Silicon Labs 指派制作一些圣诞小玩意分发给同事。虽然委托单位被设计成简单的电池和 LED 事务，但他决定自己制作一个带铃铛和口哨的。他的[马里奥主题圣诞装饰品](http://www.njneer.com/ornament-2015/christmas-ornament-2015/)使用了硅实验室 FM972 微控制器、电容感应、PWM 控制的 8 位音频和闪光灯。

有趣的部分是他使用的一些建造技术。指接式立方体由电路板制成。面板之间的电气连接使用焊料毛细铜编织物布线。这是一个有趣的技巧，我们会和一些我们最喜欢的 PCB 的创造性结构用法一起记住。

立方体的顶部有四个 LED，照亮立方体四个侧面的马里奥“问号”符号，而底部包含所有的电子设备。基片的外部是一个大的铜平面，作为电容传感元件。这意味着所有电子器件都需要表面安装，走线在一侧，这带来了一些布局挑战。由于内部设计团队的支持，添加电容检测功能变得轻而易举。微控制器的 PWM 输出负责音频，输出通过缓冲器路由以增强信号。然后，带通滤波器在将 PWM 输出馈入扬声器之前对其进行清理。

一个很好的技巧是将 24.5 MHz 音频 PWM 的时钟频率设置为 22.1 KHz，这是最初的 NES 超级马里奥兄弟的音频剪辑的采样频率。每次中断时，下一个 PWM 值从存储器载入控制 PWM 有效宽度的寄存器。因为微控制器没有足够的内存，所以增加了一个 EEPROM。[Wills]必须编写一些自定义代码，以允许将数据写入 EEPROM，并创建一个文件系统，以允许从内存中检索音频样本文件。

在立方体外面，贴上了一个激光切割的丙烯酸“硬币”。触摸瓶盖感应板时，LED 灯亮起，扬声器播放硬币声音。看看这个记录了他身材的相册和展示他身材的短片。

 [https://www.youtube.com/embed/BqYJo19Bk0Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BqYJo19Bk0Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


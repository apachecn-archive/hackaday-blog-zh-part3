# 机器人长笛口哨 MIDI

> 原文：<https://hackaday.com/2017/01/23/robo-flute-whistles-midi/>

我们不确定这在技术上是否符合音乐合成的标准，但是你还能把电脑播放音乐称为什么？在这种情况下，计算机是一个小东西，音乐来自一个普通的教室乐器:[一个塑料录音机](http://www.instructables.com/id/Automatic-Flute/)。错误的“长笛”标签来自原始项目。这个奇妙的装置使用螺线管来操作 3D 打印的“手指”和气泵——这对于录音机来说更容易，因为(不像长笛)它只需要合理的气压来产生声音。

使用 Teensyduino IDE 编程的 Teensy 3.2 驱动螺线管。该板读取从 PC 通过 USB 发送的 MIDI 命令，并将其转换为这款出色的驱动板的命令。它通过端子板将 TIP31C 晶体管和反激二极管连接到电磁阀。

在电脑上，一个名为 Ableton 的程序将 MIDI 信息发送给青少年。MIDI 信息有三个部分:一个设置信息类型和通道，另一个设置力度，还有一个设置音高。这里的代码只关注音高。

这是那些没有 3D 打印机会困难很多的项目之一。还有其他方法来启动指孔，但能够制作一个精确配合的支架非常有用。唉，我们找不到视频演示。如果你知道其中一个，请在下面的评论中删除链接。

我们已经见过[风笛机器人](http://hackaday.com/2009/05/29/mcblare-a-robot-bagpipe-player/)(事实上，我们已经见过[几个](https://hackaday.com/2017/01/10/ardu-mcduino-plays-the-bagpipes/))。我们还见过把[猎枪打成笛子](https://hackaday.com/2017/01/01/mechano-robotic-flute-made-from-an-old-shotgun/)，这当然比犁头更悦耳。
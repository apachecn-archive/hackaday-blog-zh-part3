# 青少年设计树莓派

> 原文：<https://hackaday.com/2017/09/05/teenage-engineering-the-raspberry-pi/>

十几岁的工程 OP-1 是一个微小的，便携式合成器加载了 4 轨录音，采样器，音序器，和一个相当不错的合成引擎。它也适合放在你的口袋里，看起来像西德制造的计算器。正如你对合成器/采样器/音序器的期望，你可以将声音、音轨和其他创作保存到电脑中。我想如果你能把它连到笔记本电脑上，你也可以把它连到树莓派上。他只使用一个 Pi 和一个小字符 LCD 为 OP-1 [创建了一个一体化存储解决方案。](https://www.operator-1.com/index.php?p=/discussion/3645/created-an-on-the-go-way-to-sync-my-op-1-with-a-raspberry-pi-using-a-lcd-screen-for-input-output)

将 Pi 连接到 OP-1 的过程非常简单。首先，将 USB 电缆插入 OP-1 和 Pi。然后，将 OP-1 置于磁盘模式，这是 synth 在自身和计算机之间传输文件的方法。然后，Pi 进行同步，将其字符显示的颜色从红色变为绿色，并成为一个可通过 WiFi 访问所有文件的网络服务器。

这是让文件进出 OP-1 所需的最低限度的技术。你所需要的只是一点电源和一个 USB 连接，OP-1 上的所有文件都可以备份、传输或替换，而无需任何其他浪费。它非常适合极简的 OP-1，也是一个很好的例子，说明支持 WiFi 的 Pi 是多么方便。

谢谢[Pator]送来这个。
# 如何处理旧液晶显示屏:黑掉你自己的电致变色玻璃

> 原文：<https://hackaday.com/2015/10/10/what-to-do-with-old-lcd-screens-hack-your-own-electrochromatic-glass/>

电致变色玻璃有一些科幻小说般的东西。一挥手或一个声音命令，窗口就会变暗(或变透明)。你可以得到今天这样的玻璃，或者如果你喜欢，你可以在现有的玻璃上添加(昂贵的)薄膜。

[Artem Litvinovich]二十年前就想过用液晶显示器做窗玻璃，但是成本太高了。他最近意识到，他可以很容易地从坏掉的笔记本电脑中取出液晶显示器，于是决定看看它是否可以作为一个小窗口。

拆下屏幕后(有很多拆的图片)，[Artem]需要找到 LCD 连接器上的偏置电压引脚。他将一个 12V 的电池组接地，并在正极引线上放了一个 10K 电阻。然后他触摸图钉，直到面板的不透明度有了轻微的变化。

一旦他确定了正确的引脚，他就移除其他导体，以防止电流从剩余的电路中流出。它还可以防止板载驱动器试图控制面板和干扰外部施加的偏置电压。

电子窗帘不会消耗太多电力，但它们也不会完全透明(你可以在下面的视频中看到演示)。尽管如此，一个有趣的黑客，也许有人可以改进。与用 FPGA 驱动 LCD 相比，这看起来是一个相当简单的黑客行为。当然，找到偏置线比[对整个显示屏进行逆向工程](http://hackaday.com/blog/page/2/?s=lcd)更容易。

 [https://www.youtube.com/embed/qJ-S2BYGF5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qJ-S2BYGF5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


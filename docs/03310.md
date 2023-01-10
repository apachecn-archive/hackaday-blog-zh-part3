# 采用 Raspberry Pi 触摸屏的电容成像

> 原文：<https://hackaday.com/2016/08/18/capacitive-imaging-with-a-raspberry-pi-touch-screen/>

如今，我们一直在使用触摸屏，尽管我们都知道它们支持多点触摸事件，但我们很容易将它们视为理所当然，忘记它们本身就是一个相当完善的传感器阵列。

[Optismon]长期以来一直对电容式触摸屏传感器感兴趣，最近他将注意力转向了官方的 Raspberry Pi 7 英寸触摸屏显示器。他开始读取它的原始电容值，最终得到了一个全功能的 2D 电容成像设备，能够感知隐藏在干墙中的钉子和木制品。

然而，读取电容值并不是胆小的人的工作。有一个 I2C 总线是由 Pi GPU 而不是处理器处理的，在软件中读取它需要对 Pi 臭名昭著的 Broadcom 二进制 blob 进行更改。他的解决方案(他也认为不是最佳方案)是采用另一条他可以与之对话的 Pi 的 I2C 线，并将其与显示线并联。因此，他可以捕捉到屏幕传感器的读数，并通过一点脚本在屏幕上显示 2D。当他把桌子上的手和物体放在屏幕上时，可以清楚地看到它们的轮廓，当他在墙上运行该设备时，它会显示干墙后面的墙钉和钉子的位置。

他[将他的代码发布到了 GitHub 库](https://github.com/optisimon/ft5406-capacitive-touch)，并上传了他的电容成像视频，你可以在视频中间观看。

 [https://www.youtube.com/embed/j5DztX6e-d8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j5DztX6e-d8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们之前已经报道过[大量的电容式触摸项目](https://hackaday.com/tag/capacitive-touch/)，但这是我们见到的第一台相机。现在我们知道这是可以做到的，我们期待着我们确信将来自更广泛的社区的改进。这可能成为黑客项目中一种有趣的成像技术。
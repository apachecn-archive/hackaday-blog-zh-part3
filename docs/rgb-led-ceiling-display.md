# RGB LED 天花板显示器

> 原文：<https://hackaday.com/2015/12/20/rgb-led-ceiling-display/>

迪斯科舞厅已经过时了。[dennis1a4]将它们颠倒过来，使用一些简单的硬件和大量的人力，建造了一个令人敬畏的 [RGB LED 天花板显示器](http://projectlocker.ca/otherentry.php?id=8)。他的主房间天花板正好是 32 英尺 x 20 英尺，使用 2 平方英尺。他认为他可以用 160 个 WS2812B RGB LEDs 做成一个漂亮的格子。一个安装在天花板上的 Teensy 完成所有繁重的工作，它连接着两个串行蓝牙模块。这些连接到两个蓝牙 NES 游戏控制器。每个 NES 控制器都装有一个 Arduino Pro Mini、一个蓝牙模块、锂离子电池和一个 USB 充电控制器。

蓝牙处于非安全模式，允许他连接到 Teensy，并控制 led，从其他设备除了 NES 控制器。Teensy 安装在天花板的中央，以确保良好的蓝牙连接。编程需要大量的思考和时间，但他确实设法将动画和流行游戏如贪吃蛇和俄罗斯方块纳入其中。

困难的部分是连接所有的 160 个 LED 像素。[dennis1a4]没有将 5050 SMD LED 安装在 PCB 上，而是以“死虫”方式将它们全部连接起来。每个像素有一个 LED、一个 100nF 去耦电容和与数据输入和数据输出引脚串联的 91 欧姆电阻，这些显然有助于防止数据总线上的“振铃”。检查他的激进焊接方法的视频。每个 SMD LED 都被夹在机器车间的老虎钳中，其他三个预先形成引线的部件被直接焊接到 LED 引脚上。

另一项繁琐的任务是规划和布置线束。首先在工作台上将 10 个发光二极管连接起来。然后他把它们钉在天花板上，焊接在 14 号主线束上。最后一部分是把吊顶和关闭 2 平方。制成不透明塑料网格。

[dennis1a4]做了一些试验，以确定每个 LED 和面板之间的正确距离，确保它们得到充分照明，而不会有大量光线渗入相邻的面板。这使得他不用在瓷砖之间使用挡板就能逃脱。

查看视频，看看整个构建的一个很酷的时间推移。

 [https://www.youtube.com/embed/NNvcA1aqkGU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NNvcA1aqkGU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


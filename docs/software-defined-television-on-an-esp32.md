# ESP32 上的软件定义电视

> 原文：<https://hackaday.com/2018/02/22/software-defined-television-on-an-esp32/>

单板电脑的复合视频？大问题——每一代的 Raspberry Pi 都有某种方式将复合信号输出到您选择的复古显示器上。但是 ESP32 的合成视频呢？[那也是现在的事情](http://bitluni.net/esp32-composite-video/)。

当然，有一些限制，尤其是找到一个可以接受复合输入的显示器，但由于[bitluni]的黑客没有使用额外的组件，我们可以忽略这些。这真的就像把显示器接到 25 号针和地一样简单，因为就像[他最近的 ESP32 AM 广播电台](http://hackaday.com/2018/01/28/esp32-makes-for-worlds-worst-radio-station/)一样，魔力完全在软件中。对于视频，[bitluni]再次利用他的 I S 调整将大量数据快速推入 DAC，再现 PAL 复合标准 0-1 伏范围内的同步和图像信号。他的代码也支持 NTSC 标准，但遗憾的是，由于硬件的频率限制，至少目前这两种标准都是单色的。他还通过在 ESP32 的独立内核上运行视频信号生成和 3D 渲染来提高性能。看看下面视频中的结果。

看起来 ESP32 正在成为“有什么是它做不到的吗？”系统。除了广播和视频，我们还见过[音频回放](https://hackaday.com/2018/02/06/esp32-we-have-ways-to-make-you-talk/)、[矢量图形](https://hackaday.com/2017/12/23/watch-video-on-a-oscilloscope-with-an-esp32/)，甚至[一个 Basic 解释器复活节彩蛋](https://hackaday.com/2016/10/27/basic-interpreter-hidden-in-esp32-silicon/)。

 [https://www.youtube.com/embed/5t1_XNc3vNw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5t1_XNc3vNw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


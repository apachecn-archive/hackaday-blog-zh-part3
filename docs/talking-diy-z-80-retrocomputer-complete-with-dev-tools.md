# 会说话的 DIY Z-80 Retrocomputer 配有开发工具

> 原文：<https://hackaday.com/2016/09/03/talking-diy-z-80-retrocomputer-complete-with-dev-tools/>

[Scott Baker]想接手一个新的逆向计算项目。他决定造一辆 [RC2104](http://www.smbaker.com/intro-to-z80-retrocomputing) 。幸运的是，他记录了一路上的一切。除了主板，[Scott]还构建了总线监控和调试工具、前面板、实时时钟、模数转换器和语音合成器。

你可以在包含视频的 8 篇文章中跟进。他从基本套件开始:

*   CPU–Z80
*   ROM–27c 512 64kb ROM，可在 8KB 库中选择
*   RAM–62256 32 KB RAM
*   时钟–7.3728 Mhz 晶振，驱动 74HC04 hex 反相器(用于 CPU 和 UART)
*   串行 I/O–mc68b 50 UART

此外，他拿起了一块数字输入输出板。

定制板涵盖广泛的功能:

*   实时时钟(RTC)和数字输出
*   总线管理器——控制开发总线的树莓 Pi
*   总线监视器–显示地址和数据总线
*   前面板–作为 I/O 设备的开关和 led
*   单一步进器/慢速步进器——降低执行速度(没有它，总线监视器就没有多大用处)
*   语音合成器–使用 SP0256A-AL2 的 20 世纪 80 年代风格的声音

这是一个伟大的建设和设计的老式 Z-80 电脑博览会。对接口和总线操作有很好的讨论。这个系统在 1979 年已经远远超出了最先进的水平。

在之前我们已经讨论过 RC2014 [。我们甚至报道了使用古老的 SPO256 语音合成器](https://hackaday.com/2016/02/20/hacklet-96-pi-zero-contest-projects-week-3/)的[项目。](https://hackaday.com/2013/02/18/speech-synthesizing-valentine-from-1991/)

 [https://www.youtube.com/embed/5lsjD1cuq5Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5lsjD1cuq5Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


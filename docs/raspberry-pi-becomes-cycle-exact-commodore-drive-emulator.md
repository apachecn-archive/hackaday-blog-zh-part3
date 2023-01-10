# Raspberry Pi 成为 Cycle Exact Commodore Drive 仿真器

> 原文：<https://hackaday.com/2018/05/07/raspberry-pi-becomes-cycle-exact-commodore-drive-emulator/>

Commodore 1541 磁盘驱动器不同于你在现代计算机硬件中看到的任何东西。发布时，1541 的价格几乎和它所附的 Commodore 64 一样高(400 美元，按今天的价值计算约 1040 美元)。这个驱动器有一个中央处理器，并有自己的内置操作系统。当然，现在任何使用 Commodore 64 的人都不会处理这个驱动器——你可以花 20 美元买一个 SD2IEC，从 SD 卡上下载你所有的 C64 游戏。如果你很便宜，总有磁带机接口和 10 美元的苹果闪电到 3.5 毫米耳机适配器。

但是 SD2IEC 并不能兼容所有的东西，使用磁带机拼凑东西也没有真正商品化所需的华丽。真正需要的是对 1541 磁盘驱动器的周期精确模拟，模拟这个古老磁盘驱动器中的 6502 CPU 和两个 6522 过孔。[树莓派前来救援](https://cbm-pi1541.firebaseapp.com/)。[Steve White]创造了 Pi1541，它是运行在树莓 Pi 3B 上的 Commodore 1541 磁盘驱动器的模拟。

Pi1541 完全模拟了 Commodore 1541 磁盘驱动器中的 6502 和两个 6522。它运行与磁盘驱动器相同的代码，并支持所有快速加载程序、演示和可用于原始驱动器的受拷贝保护的原始磁盘映像。

将 Raspberry Pi 3 变成 1541 所需的唯一硬件是几个双向逻辑电平转换器形式的晶体管和一个六引脚串行端口电缆插头。这可以很容易地用一些 Sparkfun、Adafruit、Amazon 或全球速卖通的部件来构建，尽管我们怀疑任何人都可以在不到一个小时的时间内用相同的电路制作一个树莓派帽子。在 Raspberry Pi 上运行 Pi1541 所需的二进制文件可以在[Steve]的网站上找到，他很快就会发布源代码。

对于逆向计算场景来说，这是一个伟大的项目，尽管有一个小小的缺点。Pi1541 需要 Raspberry Pi 3，不适用于 Raspberry Pi Zero。这将是一个了不起的软件，因为 10 美元的零件就可以完全模拟一个 Commodore 磁盘驱动器。也就是说，你仍然有可能在 50 美元以下的部分，你不会找到一个更好的驱动模拟器。

 [https://www.youtube.com/embed/6fVacXNkx7E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6fVacXNkx7E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


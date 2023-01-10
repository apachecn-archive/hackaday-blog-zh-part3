# 有机发光二极管黑了电力银行

> 原文：<https://hackaday.com/2017/09/29/oled-hacked-power-bank/>

在一次过度设计的壮举中，[Everett Bradford]侵入了他的电源库，通过有机发光二极管显示器添加了电源监视器，以显示实时电流、电压、温度和容量信息。这个想法是在他了解了 INA219 芯片后产生的。INA219 是一款分流和电源监控器 I C，具有 IC 或 SMBUS 兼容接口。该器件能够监控分流压降和总线电源电压，转换时间和滤波可编程。可编程校准值与内部乘法器相结合，能够以安培为单位直接读取电流。一个附加的乘法寄存器以瓦特为单位计算功率。

凭借令人印象深刻的小型化技能，[Everett]拆解了小米 mi 电源库，并设法添加了一个定制的电源监控模块和一个有机发光二极管显示器。不仅如此，他还更换了作为电池电量指示器的 4 个 led，实际上消耗的电流比他的主板和显示器还要多。活动时，电路板功耗约为 8mA。在睡眠模式下，功耗低于 30 A。

32×64 有机发光二极管显示器和定制电路已组装好，并紧紧地装在原外壳中。现在，电源组可以在一个小图表中显示电池电量、数字电流输入/输出、电压和温度。显示屏与电源的无缝集成让它看起来像是完全来自商店的东西。这不是典型的 [DIY 电源库](https://hackaday.com/2017/05/21/diy-usb-power-bank/)也不是[巨型 64 电池电源库](https://hackaday.com/2017/09/27/monstrous-usb-power-bank/)。这是对现有产品的精确和仔细的修改，增加了价值、功能，我敢说，风格:一个可怕的黑客！

我们可以在下面的视频中看到[Everett]的过程:

 [https://www.youtube.com/embed/0VnTvev33r0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0VnTvev33r0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


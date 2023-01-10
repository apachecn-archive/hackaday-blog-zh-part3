# 在 Python 中仿真 ICs

> 原文：<https://hackaday.com/2017/09/26/emulate-ics-in-python/>

大部分想模拟逻辑 ic 的人都会用 Verilog，VHDL，或者系统 Verilog。不是【hsoft】。他想使用 Python，并为此编写了一个简单的 Python 框架。你可以在 [GitHub](https://github.com/hsoft/icemu) 上找到代码，还有一个 ASCII 视频不会在 Hackaday 上嵌入，但你可以在[ASCII EMA](https://asciinema.org/a/WsYhXc1VcgfmkKZ8SAT18xYjv)上观看。

在断点下方，我们有一个使用 ICemu 在 Python 中“构建”电路的示例:

```
dec = SN74HC138()
sr1 = CD74AC164()
sr2 = CD74AC164()
mcu_pin = OutputPin('PB4')

sr1.pin_CP.wire_to(dec.pin_Y0)
sr2.pin_CP.wire_to(dec.pin_Y1)
sr1.pin_DS1.wire_to(mcu_pin)
sr2.pin_DS1.wire_to(mcu_pin)

print(dec.asciiart())
     _______
   A>|- U +|>Y7
   B>|-   +|>Y6
   C>|-   +|>Y5
 G2A>|-   +|>Y4
 G2B>|-   +|>Y3
  G1>|+   +|>Y2
  Y0<|-___+|>Y1
```

注意,+和–符号表示引脚的当前状态。

有用吗？看情况。如果您正在使用 Python 或者试图与其他 Python 代码集成——甚至是与 Python 绑定的另一种语言——它可能会有用。另一方面，如果你没有理由使用 Python，你可能会通过学习 [Verilog](https://hackaday.com/2015/08/27/learning-verilog-for-fpgas-hardware-at-last/) 或另一种常规硬件定义语言来获得更多的帮助、示例和工作。如果你坚持，你可以考虑使用 Python，它至少可以[合成为 FPGA](https://hackaday.com/2012/06/13/myhdl-python-programming-option-for-fpga/) 。
# MicroLisp，AVR 的 Lisp

> 原文：<https://hackaday.com/2016/09/13/microlisp-lisp-for-the-avr/>

我们以前见过基于微控制器的微型计算机，[，但没有像这样的](http://www.technoblogy.com/show?1GX1)。通常的 AVR + display + serial connection 以 BASIC、Forth 或另一种被计算机历史遗忘的语言为特色，这个项目将 AVR 变成了 Lisp 机器。

μλ项目是几十年来在大学主机上玩 lisp，在*字节*中为 6800 找一个 Lisp 解释器，用 Macintosh 工具箱写几个 Lisp 应用程序的产物。虽然这一经历使作者能够在内存受限的系统上运行 Lisp，但 MicroLisp 是在具有 32k 闪存和 2k RAM 的 ATMega328 上运行的。在那个狭小的空间里，这台微型计算机可以闪烁几块板，向有机发光二极管显示器写入数据，并读取 PS/2 键盘。

电路很简单，可以安装在试验板上，但真正的诀窍是固件。它支持 Lisp 的大部分功能，如模拟和数字读取、模拟和数字写入、I2C、SPI 和串行接口。这是一个令人惊叹的作品，它只是乞求被拼凑在一块 perfboard 上，如果只有一个口袋大小的 Lisp 机器就好了。

谢谢你的提示。
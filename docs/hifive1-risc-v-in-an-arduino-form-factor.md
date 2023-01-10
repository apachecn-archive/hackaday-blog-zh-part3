# HiFive1:采用 Arduino 外形的 RISC-V

> 原文：<https://hackaday.com/2016/11/29/hifive1-risc-v-in-an-arduino-form-factor/>

RISC-V ISA 最近越来越受欢迎——几乎就像现在正在举行一个会议一样——这要归功于这个指令集是开放的。这种开放性允许任何人构建自己的软件和硬件。当然，到目前为止，拿到 RISC-V 芯片有点困难。你可以去 opencores，找些 VHDL，在 FPGA 上运行 RISC-V 芯片。上周， [OnChip 发布了真实的、有形的硅芯片 RISC-V Open-V](http://hackaday.com/2016/11/22/mrisc-v-the-first-open-source-risc-v-microcontroller/) 。

选择总是一件好事，现在 SiFive，一家无晶圆厂半导体公司，[发布了 HiFive1](https://www.crowdsupply.com/sifive/hifive1) ，作为众筹活动。这是一个 RISC-V 微控制器，完全开源，封装在非常方便的 Arduino 外形中。

HiFive1 的核心是 SiFive 的 FE310 SoC，这是一个运行频率为 320+ MHz 的 32 位 RISC-V 内核。就外设而言，HiFive1 具有 19 个数字 IO 引脚、一个 SPI 控制器、9 个 PWM 引脚、一个外部 128 兆位闪存和*5 伏 IO。*在性能方面，HiFive1 明显快于英特尔 Curie 驱动的 Arduino 101 或 ARM Cortex M0+驱动的 Arduino Zero。根据众筹活动，支持 Arduino IDE 是包括在内的。单人间的价格是 59 美元。

因为这是一个开源芯片，你会期望关于它的一切都是可用的。SiFive 在 GitHub 上拥有从 SDK 到 RTL [的所有东西。这是开放硬件生态系统中令人印象深刻的发展，当这些芯片进入世界时，我们将会看到这一点。](https://github.com/sifive/freedom)
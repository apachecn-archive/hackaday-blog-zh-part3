# 小型封装中的 STM32 和 FPGAs

> 原文：<https://hackaday.com/2016/07/11/stm32-and-fpgas-in-a-tiny-package/>

慢慢的，非常慢的，我们不让嵌入式初学者受制于 AVR 和 PICs 的时候就要到了。FPGA 开发平台正以极其缓慢的速度变得越来越强大，越来越便宜。[Eric Brombaugh]已经在双臂和 FPGAs 上玩了一段时间了，他决定将这两种爱好结合到一块能够做很多事情的单板上。

该板被恰当地称为 STM32F303 + ice5 开发板，并完全按照 tin 上所说的那样工作。板上有一个 [STM32F303](http://www.st.com/content/st_com/en/products/microcontrollers/stm32-32-bit-arm-cortex-mcus/stm32f3-series/stm32f303.html?querycriteria=productId=LN1531) 提供一个运行在 72 MHz 的 32 位 CPU，48 kB 的 SRAM，四分之一兆的闪存，以及足够让任何人满意的外设。该板的 FPGA 侧是一个[点阵 iCE5](http://www.latticesemi.com/en/Products/FPGAandCPLD/iCE40Ultra.aspx) ，具有大约 3k 个查找表(lut)和一次可编程非易失性配置存储器。

ARM 和 FPGA 之间的连接包括一个专用 SPI 端口，以及足够的 GPIOs 来实现全双工 I2S 和 USART。像所有好的项目一样，[Eric]已经分享了所有的文件、图表和 BOMs，这些都是使这个板成为你自己的现实所需要的，并且提供了一些开发工具链的链接。虽然 FPGA 来自 Lattice 的 ice40 系列，但它不受[开源项目 Icestorm 工具链](http://hackaday.com/2015/05/29/an-open-source-toolchain-for-ice40-fpgas/)的支持。尽管如此，对于 ARM 和 FPGA 开发来说，它仍然是一个非常有能力的板。
# 生锈的手臂

> 原文：<https://hackaday.com/2017/05/03/rusty-arm/>

你可能听说过 Rust 是一种系统编程语言，它有以下几个方面的发展。它声称像 C 一样快，但具有保证内存和线程安全、泛型等特性，并防止分段错误。听起来很适合嵌入式系统，对吗？[Jorge Aparicio]很沮丧，因为他选择的 STM 32 ARM Cortex-M CPU 不支持 Rust。

显然，你可以很容易地将 C 函数绑定到 Rust 程序中，但这不是他想要的。因此，他着手构建可以访问设备硬件的纯 Rust 程序，并记录了这一努力。

帖子不仅向你展示了你需要的工具和软件版本，而且使用 OpenOCD，[Jorge]甚至设法做了一些调试。这项技术似乎也非常普遍适用，因为他说他已经在来自三个不同供应商的六个不同的控制器上完成了同样的技巧，没有任何问题。您必须通过更改模板中的一些值来配置项目。

虽然这不是一个 Rust 教程，但是跟随[Jorge 的]代码和他的解释会让你对 Rust 有一个很好的了解。他还展示了一个简洁的工具， [gdb-dashboard](https://github.com/cyrus-and/gdb-dashboard) 。为了在 ARM 的特殊内存区域构建 API，[Jorge]使用了一个名为 svd2rust 的工具来处理供应商的 svd 文件。这些通常用于 JTAG 编程和测试，所以我们认为这是一种自动构建处理器支持的新方法。

许多提供安全特性的语言倾向于编译胖代码。[Jorge]展示了一个闪烁的 LED 示例，并将其分解，它看起来非常紧凑，大约 127 个字节。然后，他抽象出定时器寄存器，代码在编译时几乎完全相同。

不久前我们短暂地覆盖了铁锈。最近我们还看到一些 [WiFi 设备](https://hackaday.com/2017/01/04/rust-running-on-the-realtek-rtl8710-esp8266-alternative/)生锈。
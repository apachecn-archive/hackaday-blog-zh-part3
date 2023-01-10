# 地平线上裸露的金属锈迹

> 原文：<https://hackaday.com/2018/03/12/baremetal-rust-on-the-horizon/>

自 2010 年由 Mozilla 宣布以来，Rust 编程语言已经取得了突飞猛进的发展。由于内存安全和所有权系统等特性，它已经成为一种非常流行的语言。现在，一个针对 Rust 的[嵌入式设备工作组的消息传来，该工作组旨在改善对微控制器](https://internals.rust-lang.org/t/announcing-the-embedded-devices-working-group/6839)的支持。

Rust 在语法方面与 C++非常相似，但是 Rust 不允许空指针或悬空指针，这对新手来说是更可靠的代码。借助这一新举措，跨不同微控制器架构的嵌入式开发可以获得更加一致和标准化的体验，从而实现开箱即用的代码可移植性。[提出的改进](https://github.com/rust-lang-nursery/embedded-wg/blob/master/minutes/2018-02-20.md)包括用于开发和设置代码生成的 IDE 和 CLI 工具。还有关于 RTOS 实现和协议栈集成的讨论，这将把社区参与提升到一个全新的水平。

这是一件真正令人兴奋的事情，因为 rust 有可能成为嵌入式开发中 C++的替代品，因为 Rust 代码运行时非常少。在 Arduino 出现之前，许多人害怕一段简单代码的结果，但有了 rust，编写内存安全的代码而不显著影响性能将成为可能。在社区的支持下，Rust 可能是一个更有效的选择。我们已经在 ARM 控制器上看到了一些基于 Rust 的成果[，如果你想开始的话，我们已经在过去介绍过](https://hackaday.com/2017/05/03/rusty-arm/)[Rust 编程的基础知识](https://hackaday.com/2015/12/18/programming-with-rust/)。硬件黑客的好日子即将到来。
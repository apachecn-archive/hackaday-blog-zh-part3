# Rust 在 Realtek RTL8710 上运行:ESP8266 替代方案？

> 原文：<https://hackaday.com/2017/01/04/rust-running-on-the-realtek-rtl8710-esp8266-alternative/>

对于简单地让您的项目连接到 WiFi，至少在黑客圈，没有什么能打败 ESP8266。但它不是唯一的参与者，我们喜欢看到我们使用的部件和语言的多样性。ESP8266 的一个大缺点是有点古怪的 Xtensa CPU。它只是不像基于 ARM 的同类产品那样受到各种工具链的广泛支持。

因此，当[扎克]想要在 Rust 中做一些嵌入式工作时，ESP8266 就不在考虑范围内了。他[转向 RTL8710](https://polyfractal.com/post/rustl8710/) ，一个由 Realtek 制造的非常相似的 WiFi 模块。目前，RTL8710 的文档很糟糕，就像黑客社区之前的 ESP8266 文档一样。但是为了弥补这个缺点，[扎克]不得不使用支持 ARM 架构的 [LLVM 编译器](http://llvm.org/)，这意味着他可以在 [Rust](https://www.rust-lang.org/en-US/) 中编码。

最后，[扎克]描述的设置混合了[FreeRTOS](http://www.freertos.org/)和一些[mbed](https://www.mbed.com/en/)库，这应该足够让你轻松地在芯片上运行了。实际上，我们自己已经订购了几个这样的模块，并且希望直接从 C 开始，但是让 Rust 示例工作并没有坏处，看起来也没有什么不同。

还有人在用[RTL 8710](http://hackaday.com/2016/07/28/new-chip-alert-rtl8710-a-cheaper-esp8266-competitor/)吗？基于 ARM 的廉价 WiFi 芯片应该会很有意思。
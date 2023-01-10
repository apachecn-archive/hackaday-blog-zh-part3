# Hackaday.io 用户评论六款 STM32 IDEs

> 原文：<https://hackaday.com/2017/04/04/hackaday-io-user-reviews-six-stm32-ides/>

开始任何基于 Arm 的项目的一个问题是选择一个工具集。我们这里的一些人只是使用命令行和我们最喜欢的编辑器，但是我们知道这并不适合很多人——他们想要一个现代化的 IDE。但是选哪个呢？用户[Wassim]面对这个问题，评估了 STM32 的六个不同选项，并好心地[在 hack aday . io](https://hackaday.io/page/3033-6-ides-to-debug-the-2-stm32-bluepill)上记录了他的发现。

许多工具只适用于 Windows，其中至少有两个不是完全免费的，但它仍然是一个很好的列表，包含了一些很好的观察。当然，IDE 的选择是高度个人化的事情，但是仅仅有一个好的列表就是一个很好的开始。

【Wassim】对 STM32 的兴趣是由[蓝色药丸板](https://hackaday.com/2017/03/30/the-2-32-bit-arduino-with-debugging/#comment-3498343)激发的——2 美元的 STM32 板和他调试它的愿望。他发现你经常需要对 ide 进行调整才能让它们工作。事实上，他的最终选择确实需要相当多的工作，这一点他也有同感。

他提到的一件事我们也注意到了:大多数 ide 依赖 st 提供的名为 CubeMX 的代码生成器来启动项目。这很方便，因为它可以让你选择 I/O 设备，并为时钟、中断、I/O 设置等构建许多设置代码。然而，如果你[试图使用 PLL 作为主时钟](https://community.st.com/thread/39340-bug-cubemx-v420-rcc-initialization-fail-with-hse-selected)，发生器中至少会出现一个 bug。修复很简单，但是您必须在每次重新生成代码时应用它。说到时钟，如果你在这个级别使用 STM32 器件，你会喜欢这个关于[时钟选项和警告](https://hackaday.com/2014/11/23/down-the-rabbit-hole-of-stm32-clock-options/)的讨论。

我们喜欢看到 Hackaday 的读者与我们分享他们的研究，如果你没有浏览 Hackaday.io，你就错过了至少一半的 Hackaday 体验。与此同时，我仍然是 Emacs 的抵制者。它甚至还处理调试。

 [https://www.youtube.com/embed/M7RBQsq5_lc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M7RBQsq5_lc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


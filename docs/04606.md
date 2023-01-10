# Atari 现在运行 Java，谢天谢地不需要不断更新

> 原文：<https://hackaday.com/2017/01/02/atari-now-runs-java-thankfully-doesnt-require-constant-updates/>

Java Grinder 是一个编译 Java 程序以在微控制器和控制台等平台上运行的工具，它通过输出本机汇编代码和使用 API 来与定制的硬件(如定制的图形和声音芯片)一起工作。在其他硬件中，Java Grinder 支持 Commodore 64，它使用 6502 CPU 的变体。[Michael Kohn]意识到 Atari 2600 共享这种处理器，并认为他可以通过扩展[乔·戴维孙]所做的 C64 工作，开始让 Java Grinder 与 Atari 一起工作。他们一起将 [Java 带到了 Atari 2600 上，并在此过程中制作了一款游戏](http://www.mikekohn.net/micro/atari2600_java.php)。

根据[Michael]的说法，项目的某些部分很简单，因为一些 Java 例程在 6502 上可以编译成 1 到 2 条指令。其他部分更难，比如处理图形子系统，修改 Java Grinder 以输出 8 位字节码来适应雅达利微小的 4K ROM 限制。即使有了这个调整，他们仍然不能适应游戏和标题屏幕。最终，他们依靠[银行转换](https://en.wikipedia.org/wiki/Bank_switching)来完成任务。[Joe]的游戏对于 Atari 2600 来说是相当可靠的——块状图形和哔哔声——他们已经将它上传到页面上，所以你可以在模拟器中亲自尝试。

最终，将 Java 代码移植到一个有 128 字节 RAM 的系统上可能不会特别有用。然而，作为一次编码练习和学习经历，在培养你的编码技能方面有很多价值。其他类似的实验向我们展示了 Java 在其他意想不到的设备上的运行，比如 Sega Genesis T1 或 T2 MSP 430 T3。休息后的视频。

 [https://www.youtube.com/embed/VN-8Z4VUjzg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VN-8Z4VUjzg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


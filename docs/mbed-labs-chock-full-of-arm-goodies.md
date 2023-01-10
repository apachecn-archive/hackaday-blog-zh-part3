# 装满 Arm 产品的 Mbed 实验室

> 原文：<https://hackaday.com/2018/01/10/mbed-labs-chock-full-of-arm-goodies/>

我们喜欢 ARM 处理器的一点是它有多种库支持选项。当然，您可以在裸机上编写自己的代码，但是您也可以使用许多不同的抽象库来简化事情。另一方面，有 Mbed，类似于 Arduino 提供的那种库。易于使用，虽然不总是最好的性能。Mbed 现在有一个 [Mbed Labs](http://labs.mbed.com/) 网站，里面有很多 Mbed 生态系统附带的额外的好东西，它有很多有趣的东西。

你总是能够在浏览器中编写 Mbed 代码——有些人喜欢这样，有些人讨厌这样，并使用本地托管的工具，如 [Platform.io](https://hackaday.com/2016/04/23/atomic-arduino-and-other-development/) 。然而，有了 Mbed 实验室，你可以在浏览器中构建并且最重要的是模拟你的代码([我们去年讨论过的](https://hackaday.com/2017/12/17/an-mbed-in-your-browser/))。还有一个运行在你的芯片上的 Javascript 解释器，一个用于深度学习的 TensorFlow 的小实现，以及页面上的其他几个项目。

模拟器令人印象深刻，因为它还包括像 LCD 显示器和温度传感器这样的外围设备模拟。我们确实希望它能与完整的 IDE 集成，但是它是开源的，并且在 [GitHub](https://github.com/janjongboom/mbed-simulator) 上，所以如果你想的话，你可以添加你自己的项目。有演示程序，从 LED 闪烁程序到 TCP/IP 网络示例。

我们发现一件令人惊讶的事情:模拟器允许你使用浏览器的调试器来调试。有一些源代码映射可以告诉浏览器你的代码，这样你就可以设置断点和进行其他的调试操作。

Javascript 解释器也很有趣，尽管你需要一个至少 64K 内存的开发设备来容纳它。然后你可以这样写:

```
var led = DigitalOut(D0);
var button = InterruptIn(D1);

button.fall(function() {
 led.write(led.read() ? 0 : 1);
});
```

所有这些代码都是开源的，有几个重要的例子。ARM 声称 Javascript 代码比 C++代码慢大约 100 倍，但由于所有底层调用仍然是 C++，这并不像听起来那么糟糕。对于许多项目来说，以几个 MIPS 运行已经足够了，这也是事实。

在实验室网页上有更多的项目，毫无疑问还会有更多。同时，如果你想了解 Mbed，你可以[从这里](https://hackaday.com/2015/08/11/getting-started-with-arm-using-mbed/)开始，然后继续[创建一个函数生成器](https://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/)。
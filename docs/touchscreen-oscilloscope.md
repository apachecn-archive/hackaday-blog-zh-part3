# 触摸屏示波器

> 原文：<https://hackaday.com/2017/08/08/touchscreen-oscilloscope/>

[Marco Reps]不想在跑步时带着全尺寸示波器到处测量心电图。他决定[看看 DSO112A](https://www.youtube.com/watch?v=fGU9LoEpQFw) ，这是一个通常来自中国的微型触摸屏。微型单通道示波器可以在 2MHz 下达到 2mV/分度，并且可以保存和调用多达 24 种配置。它还可以通过串行端口访问数据，因此您可以将它用作一个奇特的数据记录器。[Marco 的]视频出现在下面。

很明显，有一个更老的型号，末尾没有 A，不那么灵敏，还有一些其他缺失的功能。价格大约是 70 美元——相当便宜，虽然不是一次性的便宜。

[Marco]注意到两个小连接器中的一个可以作为外部触发输入或函数发生器。里面有典型的 LiPo 电池和屏蔽输入部分。[Marco]撕下板子，看着板子上的芯片。内部有两个 Atmel CPUs 和一个每秒 20 兆采样的模数转换器。

彩色屏幕在视频中看起来出奇的好，尽管正如[Marco]指出的那样，对于一个频道，颜色并不是非常有用。该设备还具有光标和一个很好的测量选择，既可以实时工作，也可以存储数据。

在视频的最后，[Marco]展示了一个简单的 ECG 放大器，他根据一个开源原理图[构建而成。如果你想了解更多，我们之前已经讨论过简单的](https://www.olimex.com/Products/Duino/Shields/SHIELD-EKG-EMG/) [ECG 电路](http://hackaday.com/2016/11/07/simple-ecg-proves-you-arent-heartless-after-all/)。

去年我们看了两个便宜的小望远镜。和其他事情一样，门槛每年都在提高。不过，公平地说，这些示波器的(报道)带宽为 25 MHz。我们希望看到 DSO112A 用户界面的这种前端。

 [https://www.youtube.com/embed/fGU9LoEpQFw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fGU9LoEpQFw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


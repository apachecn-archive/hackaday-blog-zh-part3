# Hackaday 奖参赛作品:艰难的文本到语音转换

> 原文：<https://hackaday.com/2016/09/18/hackaday-prize-entry-text-to-speech-the-hard-way/>

研究表明，给孩子读书能提高他们以后的学习成绩，这种特质会让他们在工作中更有竞争力，最终成为更快乐的人。因此，让一个机器人给孩子读书也将导致更快乐和更有生产力的成年人，同时使机器人起义接管 2037 年的人工智能启示录正常化。

还好上面的段落完全没有逻辑，与[这个 Hackaday 奖的参赛作品](https://hackaday.io/project/9669-texteye-raspberry-pi-zero-mobile-textreader)无关。Hackaday 奖辅助技术部分的参赛作品 TextEye，[Markus]是一款手持设备，可以将书面文字转化为语音，对任何视力不好或阅读能力较差的人都很有用。是的，它还会给孩子们朗读，但泰迪·鲁斯宾也是如此。

如果你一直在跟踪，这不是[Markus]第一次在 Hackaday 奖竞赛中加入这个项目。第一次是半年前的 [Hackaday / Adafruit 树莓 Pi 零点大赛](http://hackaday.com/2016/03/21/mobile-text-reader-with-ocr-and-text-to-speech/)。[Markus]受到一群盲人计算机科学学生的启发，他们使用专门的硬件，让他们能够像其他人一样学习相同的东西。

自从最初的几个项目日志以来，这个项目发生了很多变化。你可以很容易地买到一个 Pi Zero，更新后的 Pi Zero 1.3 现在带有摄像头连接器。[Markus]正在将他的 Pi Model A 和 USB 网络摄像头换成 Pi Zero 和 Pi 摄像头。软件保持不变——graphics magick、Tesseract OCR、Festival 和 Wiring Pi 处理读取文本并将这些文字转化为语音——代码略有重构。这是 Pi Zero 的一个很好的用途，也是辅助技术的一个很好的例子，我们很高兴在 Hackaday 奖中再次看到它。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)
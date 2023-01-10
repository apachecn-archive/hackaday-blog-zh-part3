# Arduino 时钟是 HAL 1000

> 原文：<https://hackaday.com/2016/12/11/arduino-clock-is-hal-1000/>

在电影 *2001:太空漫游*中，HAL 9000——神经兮兮的计算机——在 1992 年过了生日(出于某种原因，在书中是 1997 年)。在 20 世纪 60 年代末，这个日子听起来遥远得不可思议，但现在似乎成了遥远的记忆。唯一的问题是，我们现在才开始得到实用的带声音输入输出的计算机，尽管它们离 HAL 还很远。

[GeraldF6]构建了一个基于 Arduino 的时钟。这并不新鲜，但多亏了 MOVI 板(好吧，盾牌)，这个时钟有语音输入和输出，正如你在下面的视频中看到的。与大多数现代语音设备不同，MOVI 板(以及时钟)根本不使用云中的外部服务器或任何远程处理。另一方面，语音质量并不是你所期望的现代智能手机助手所能提供的。我们估计它可能是 HAL 9000 的 1/9。

你可能想知道你要对一个钟说什么。您将在视频中看到，您可以设置和查询计时器。与哈尔不同，该设备的工作原理类似于《星际迷航》中的电脑。你称呼它为 Arduino。然后它会发出哔哔声，你就可以说出命令了。还有一个实时时钟模块。

设置 MOVI 很简单:

```
 recognizer.init(); // Initialize MOVI (waits for it to boot)
 recognizer.callSign("Arduino"); // Train callsign Arduino (may take 20 seconds)
 recognizer.addSentence(F("What time is it ?")); // Add sentence 1
 recognizer.addSentence(F("What is the time ?")); // Add sentence 2
 recognizer.addSentence(F("What is the date ?")); // Add sentence 3
...

```

然后对 recognizer.poll 的调用将为它听到的任何内容返回一个数字代码。下面是一个片段:

```
// Get result from MOVI, 0 denotes nothing happened, negative values denote events (see docs)

 signed int res = recognizer.poll(); 

// Tell current time
 if (res==1 | res==2) { // Sentence 1 & 2
 if ( now.hour() > 12) 
 recognizer.say("It's " + String(now.hour()-12) + " " + ( now.minute() < 10 ? "O" : "" ) +
     String(now.minute()) + "P M" ); // Speak the time
...
```

相当容易。

哈尔是美国宇航局的项目 *(USSC，不是美国宇航局，哈尔是伊利诺伊大学香槟分校* *实验室的产品。)*可能要花几百万，但 MOVI 板要 70-90 美元。它也不太可能发疯并试图杀死你，所以这是另一个好处。也许我们会在[造一个不同的外壳](https://hackaday.com/2016/11/15/put-an-honest-face-on-alexa-with-this-hal-9000-build/)。我们最近谈到了[神经网络改善语音识别和合成](https://hackaday.com/2016/12/03/talking-neural-nets/)。这与那相差甚远。

 [https://www.youtube.com/embed/-INEf4BjQgM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-INEf4BjQgM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


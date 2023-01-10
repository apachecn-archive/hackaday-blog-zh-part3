# 制造便携式太阳能点焊机:超级电容器充电

> 原文：<https://hackaday.com/2018/02/28/building-a-portable-solar-powered-spot-welder-charging-supercapacitors/>

在农历新年之前，我从中国订购了两个 3000 F，2.7 V 的超级电容器，每个大约 4 美元。我实际上不记得为什么，但他们在假期前(出乎意料地)到达了。

超级电容器(通常称为超级电容器)填补了可充电锂电池和普通电容器之间的空白。普通电容器的能量密度低，但功率密度高:它们可以非常快速地储存和释放能量。锂电池储存大量能量，但充电和放电速率相对较低。按重量计算，超级电容器储存的能量比锂电池少 10 倍，提供的功率比电容器低 10 倍左右。

[![](img/5edeba3aa14fa2d32702543419680ef7.png)](https://hackaday.com/wp-content/uploads/2018/02/supercapacitors_chart2.jpg)

总的来说，它们是一种奇怪的技术。尽管有热情的新闻报道，但它们是电池或电容器的糟糕替代品，但它们的长寿命和适中的能量和功率密度使它们本身适合一些简单的应用。值得注意的是，它们被用于[能量收集](http://hackaday.com/2017/05/15/hackaday-prize-entry-self-sustained-low-power-nodes/)，再生制动，延长汽车铅酸电池的寿命或者[替换汽车铅酸电池](http://hackaday.com/2014/10/18/replacing-the-lead-in-a-motorcycle-battery-with-supercaps/)，以及[在某些类型的存储器中保留数据](http://hackaday.com/2015/10/19/mostly-non-volatile-memory-with-supercapacitors/)。你不太可能用超级电容器给你的笔记本电脑供电。

反正我放了一周的假，还有两个来历不明的大电容。有时我们生活在所有可能的世界中最好的一个。

据称，每个电容器能够储存大约 11 千焦的能量，并以惊人的速度释放能量。确切的比率是多少还不清楚，因为我没有任何关于内部电阻，耐热性，甚至极性的文件。

更复杂的是，在接下来的两周左右，我所有的供应商都关门了。无论我要建造什么，第一个挑战是它必须从手头的零件开始建造。其次，目前大多数医院都在减少产能，因此比以往任何时候都更加安全。

出于这个和其他原因，定向能武器是不可能的。(请用科学换和平！)不过，我确实需要一台点焊机，而且不乏有人用超级电容器自制的例子，通常在 500 华氏度范围内。

 [https://www.youtube.com/embed/0FZVzVo8gLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0FZVzVo8gLM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



然而，我使用了六倍的容量，并且我不觉得这些构建中使用的安全预防措施(大多数情况下没有)有特别好的伸缩性。我主要关注两个方面:安全有效的充电方法，以及防止意外放电。

后者很容易修复。由于超级电容器的形状大致相当于一个大型电池，所以我在一个电极周围放了一个环作为隔离物。胶带不是结构性的，它只是为了拍照和插入电容器时将塑料固定在适当的位置。

[![](img/2ec7c91f0cb06c1a6dd1bd0a9d3815ac.png)](https://hackaday.com/wp-content/uploads/2018/02/capacitor-spacer_thumbnail.png)

No datasheet, specifications, or polarity indicators. Seems legit.

然后，我用一个防风雨的塑料盒和一些 0.7 毫米厚的铜板制作了一个大型的 AA 电池座。稍后，我会在这些板上钻孔，并用螺栓连接粗铜线。我也可以用防火的东西，比如沙子，来填充围栏里的空间。

电容器安装牢固，我无法通过大力摇晃外壳将其取出。下一个挑战是确定电容器的极性，这样我就可以在外壳上清楚地标记出来。出于习惯，我拿出一个万用表，测量端子之间的电压，没有意识到这可能不起作用。

不幸的是，它确实起作用了。有人决定运输含有大量电荷(约 1 伏)的超级电容器。当我收到它们的时候，它们包装得很好，但是我仍然想不出有什么理由他们会运输它们并承担费用。如果我们的读者能想到一个，请在评论中告诉我们！

## 冲锋！

无论如何，现在我可以或多或少安全地储存和连接东西到电容器上了，是时候做一个充电器了。当然，YouTube 上有许多这样的例子:人们手动连接和断开锂电池和限流电阻，同时还拿着万用表，或者连接具有限流功能的大型变压电源。还有电压限制和电池平衡超级电容器保护板，这是一个非常合理的选择，但我的供应商没有携带它们，并在接下来的 2 周内关闭。

直接使用电池是不可能的。限流电阻会浪费大量电力，人为错误会导致电容过度充电或极性错误，从而缩短其寿命(我也可能如此)。大型电容器故障状态似乎在“大型鞭炮”和“小型手榴弹”之间变化，这两种我都不太喜欢。一个大电流的台式电源也不太好，因为它需要一个墙上的插座，我希望把它做成一个移动设备。

我有几个额定电流为 5 A 的 DC-DC 降压转换器。它们的效率相当高，约为 85%，可以输出低至 0.8 V 的电压，DC 输入约为 5-32 V。我打算为此提供一组不同电压的锂电池、一个 40 W 18 V 的太阳能电池板，以及旧笔记本电脑电源等其他电源。

我拆开了一个坏掉的 DC-DC 转换器，看看它用的是什么芯片。那是一辆 [XL4005E1](http://www.xlsemi.com/datasheet/XL4005%20datasheet.pdf) (PDF)。数据手册上说它有一个“100%的最大占空比”(原因我们将在后面讨论)，并有一个高电平有效使能引脚。这似乎是一个利用[脉宽调制](http://en.wikipedia.org/wiki/Pulse-width_modulation)将电源输出电流限制在安全电流范围内的好方法。

![](img/84aeefe7bb0921f4568da38b8361db37.png)

Set to very low duty cycle during testing.

虽然 555 定时器已经足够了，但我使用了 ESP8266，因为我计划以后扩展功能。电容器充电时充电速率变慢，因此理想的 PWM 占空比取决于当前的充电水平。后来，我想使用 ESP8266 上的板载模数转换器来优化充电速率，使用 LED 或屏幕显示充电状态，并在充电时自动关闭电路以节省电能。目前，唯一的目标是找到一个合理的占空比，将超级电容器充电到 2 V 以上进行测试。为此，我将输出设置为 2.5 V，并将 ESP8266 的 PWM 输出连接到 XL4005E1 使能引脚。PWM 输出由 ESP8266 上的以下简单程序决定:

```
pwm.setup(1, 1000, 650)
pwm.start(1)
```

可惜这根本没用。XL4005E1 一直开着，谢天谢地，它在任何燃烧发生之前就关闭了。将使能引脚接地或 VCC 也没有效果——我怀疑是一个伪造的芯片。具有讽刺意味的是，数据手册上说它有“最大 100%占空比”仍然是完全正确的，结果发现这也是最小占空比！

[![](img/6cc304be968b52d3c20faf518338209c.png)](https://hackaday.com/wp-content/uploads/2018/02/led-dimmer_thumbnail.png)

我四处寻找可以转换足够电流的东西，作为一种有用的替代品。我发现了一叠有人让我给他们买的 LED 调光器，一直没拿起来。它们非常便宜，我很高兴我现在还留着它们。在里面，我发现了一个 9 V 电压调节器、一个 555 定时器和一个带散热器的 IRF530N 功率 MOSFET (PDF)。

我不禁想到，如果只是把 9 V 的稳压器去掉，就可以直接用调光器来控制电源的输出电流了。然而，这将意味着以后没有自动控制，表盘没有任何特别有用的标记。

我将 MOSFET 脱焊，并使用 3.3 V 输出来驱动栅极。数据表表明这可能不会工作，坦率地说，我不应该打扰。最终起作用的是通过一个 2N2222 晶体管将 DC-DC 调节器的输入端(对于我的用例，它将始终是 7.4-18V)连接到 MOSFET 栅极。晶体管的基极连接到 ESP8266 PWM 输出。PWM 输出允许晶体管切换 DC-DC 调节器输入，从而有效驱动功率 MOSFET。

我之前发现，如果电流超过 8 A，DC-DC 转换器就会关闭。通过反复试验，我发现 40%的占空比工作得很好，同时安全地考虑了供应商的乐观情绪。缺点是，在占空比固定的情况下，当电容达到约 2.15 V 时，充电速率几乎为零。我的测试目标是将其充电至 2 V，因此目前这是可以接受的。为了方便起见，我附加了一个小型 LCD 电压表来监测电荷，并称之为足够好了。

[![](img/3d01ffd35c9df73c0de3597660e933e9.png)](https://hackaday.com/wp-content/uploads/2018/02/finished_kludge.png)

Black case mostly added so I don’t have to look at my ugly circuit.

不可否认的是，在对电路进行了一些计划外的修改后，这变得有点像是由零件组装而成的。如果我必须重做，我可能会保留由 BJT 控制的功率 MOSFET，但用 8 位 Atmel MCU 取代 ESP8266。它会更小，更节能，更便宜，我过去喜欢用 ASM 编程这些芯片。这种方法的另一大优势是，我可以使用脉冲序列来并行添加多个电源，而这在 ESP8266 上可能并不实用。通常这是不安全的——其中一个电源故障意味着其他电源很快失控。然而，如果每个电源通过其自己的功率 MOSFET 连接到超级电容器，并且微控制器管理它们，以便一次只有一个电源开启，那么它应该没问题，并以可接受的成本提供更快的充电速率。

下一步是制造电极和大电流开关，然后尝试焊接不同的材料。我还想优化充电电路。我认为这一天已经足够了，所以请继续关注即将到来的火花。

**更新:**阅读[这次太阳能点焊机冒险](https://hackaday.com/2018/03/15/building-a-portable-solar-powered-spot-welder-nearly-practical/)的结论。
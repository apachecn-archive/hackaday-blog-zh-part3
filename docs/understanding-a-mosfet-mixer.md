# 了解 MOSFET 混频器

> 原文：<https://hackaday.com/2018/06/11/understanding-a-mosfet-mixer/>

混频器接收两个信号并将它们混合在一起。结果输出通常是两个频率，加上它们的和与差。例如，如果馈入一个 5 MHz 信号和一个 20 MHz 信号，则输出频率分别为 5 MHz、15 MHz、20 MHz 和 25 MHz。在平衡混音器中，原始频率相互抵消，尽管不是所有的混音器都这样做，或者至少做得不完美。[W1GV]有一个视频解释了带[双栅极 MOSFET](https://www.youtube.com/watch?v=PJTnJUkvFvw) 的混频器的设计，您可以在下面看到。

双栅极 MOSFET 几乎是这种应用的理想选择，它具有两个独立的栅极，实际上具有无穷大的输入阻抗。[Stan]带您了解基本电路，并以白板形式解释操作。

奇怪的是，你认为混音器是将两个信号相加，但如果你考虑到其中涉及的三角学，它实际上是将两个信号相乘。考虑一个正弦波:

```
f=A*sin(ω*t+φ)
```

在该公式中，A 是幅度，ω是弧度频率(即 2 倍π乘以频率，单位为赫兹)，φ是相位(单位为弧度)。当然，t 是时间。现在，考虑两种频率:

```
f1=A1*sin(ω1*t+φ1)   f2=A2*sin(ω2*t+φ2)
```

请记住，余弦波只是相位增加了 90 度的正弦波。如果你简单地将这两个相加，你会得到 f [1] +f [2] ，但是要得到相加的频率，我们确实需要ω [1] +ω [2] 和ω [1] -ω [2] 出现在输出中。记住 sin(a)sin(b)= 1/2[cos(a-b)-cos(a+b)]—或者记不住的话[查一下](https://en.wikipedia.org/wiki/List_of_trigonometric_identities#Product-to-sum_and_sum-to-product_identities)。因此，将两个正弦波相乘会产生和频和差频的两个相移正弦波(余弦波)。这就是为什么调音台的符号中有一个 X，而不是一个加号。

除了最简单的发射机和接收机，混频器是所有发射机和接收机的基本组成部分。很多时候，你会看到人们使用集成了振荡器和混频器的 IC，如 [NE602 或 NE612](https://hackaday.com/2018/06/06/homebrew-sdr-ham-radio-in-9-parts/) 。还有其他的[芯片](https://hackaday.com/2018/04/22/an-fm-transceiver-from-an-unexpected-chip/)。

 [https://www.youtube.com/embed/PJTnJUkvFvw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PJTnJUkvFvw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


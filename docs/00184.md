# 神秘 FPGA 电路感受到压力

> 原文：<https://hackaday.com/2015/09/27/mystery-fpga-circuit-feels-the-pressure/>

您有一个 FPGA 电路，您希望用户通过按下按钮来与您的电路进行交互。很明显，你需要一个按钮，对吗？没那么快！[Clifford Wolf]最近发现了一个神秘的效果，当有人推他的冰棍板时，[可以让他察觉。](http://svn.clifford.at/handicraft/2015/ringosc/)

下面的视频显示了神秘的电路(这只是股票冰棍板)，它似乎反应任何时候你弯曲的 PC 板。Verilog 实现了一个简单的环形振荡器(基本上是一个输出与输入相连的反相器)。

以下是他的 Verilog 代码摘录:

```
// ring oscillator
 wire [99:0] buffers_in, buffers_out;
 assign buffers_in = {buffers_out[98:0], chain_in};
 assign chain_out = buffers_out[99];
 assign chain_in = resetn ? !chain_out : 0;
SB_LUT4 #(
 .LUT_INIT(16'd2)
 ) buffers [99:0] (
 .O(buffers_out),
 .I0(buffers_in),
 .I1(1'b0),
 .I2(1'b0),
 .I3(1'b0)
 );
```

他将输出频率与板载晶体振荡器的已知频率进行比较，并将较大的偏移记录为推动。起初，我们认为这可能是晶体上的机械弯曲，但如果你看视频，环形振荡器的输出在触摸时明显偏移。据推测(这是猜测)，电容和其他电路参数的微小变化会对环形振荡器的频率产生影响。[Clifford]说他有很多理论，但不知道哪一个(如果有的话)是正确的。

我们不能决定在实践中是否依赖这种效应。但在视频中似乎是可以重复的。也许[Clifford]发明了一个新的产品类别:现场可编程门阵列和开关(FPGAS)。我们已经在冰风暴项目的[之前提到过【Clifford】的工作，甚至在我们的 FPGA 教程](http://hackaday.com/2015/05/29/an-open-source-toolchain-for-ice40-fpgas/)中使用了他的[开源工具链(顺便说一句，很快会找到另一个)。](http://hackaday.com/2015/08/27/learning-verilog-for-fpgas-hardware-at-last/)

 [https://www.youtube.com/embed/UFqWjZudOho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UFqWjZudOho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示[詹姆斯·鲍曼]。
# 滚动你自己的旋转编码器

> 原文：<https://hackaday.com/2018/02/19/roll-your-own-rotary-encoders/>

[miroslavus]在旋转编码器方面运气不佳。他从通常来源测试的零件都有机械或电气问题，导致他的项目表现不佳。即使试图解决软件中的缺陷也无济于事，所以他做了任何一个充满活力的黑客都会做的事情——他用微型开关和 3D 打印部件建造了自己的旋转编码器。

[miroslavus]的“编码器”不是传统意义上的正交编码器。它有两个开关，只有其中一个在转向某个方向时会触发，一个顺时针，一个逆时针。旋钮下侧有一个棘轮，与一个小跳闸杆啮合，当棘轮移动跳闸杆时，小心定位的[微动开关](http://hackaday.com/2017/04/17/microswitches-past-the-tipping-point/)被反复启动。动作流畅，但令人满意的点击。就我个人而言，我们会放弃 3D 打印基板，转而采用带有[去抖动电路](http://hackaday.com/2015/12/09/embed-with-elliot-debounce-your-noisy-buttons-part-i/)的定制 PCB，或许会重新定位开关，使它们位于旋钮下方，以实现更紧凑的外形。再加上轴上的另一个开关来记录旋钮的推动，你就有了一个完美的导航菜单的输入设备。

我们认为这很棒，但也许你的项目真的需要一个合法的旋转编码器。在这种情况下，你会想要赶上像[格雷码](http://hackaday.com/2017/01/25/fifty-shades-of-gray-code/)这样的基础知识。

 [https://www.youtube.com/embed/I41c4Bo2q7I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I41c4Bo2q7I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


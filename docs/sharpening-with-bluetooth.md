# 使用蓝牙锐化

> 原文：<https://hackaday.com/2018/03/31/sharpening-with-bluetooth/>

厨房里很少有东西像钝刀子一样令人沮丧。[Becky]和她的厨师朋友合作建立了一个蓝牙模块，告诉你何时在最佳角度磨刀。这听起来可能有点专业，但问题归结为一个在很多情况下都足够普遍的问题:你如何在运动中判断你的准确方向？也就是说，当刀在磨刀石上快速来回移动时，如何可靠地测量刀片的角度？

寻找挑战，[Becky]的第一次尝试是只使用加速度计。它起作用了，但不是很精确。她的最终答案是一个完整的惯性测量单元——bno 055，它结合了一个加速度计、一个磁力计和一个陀螺仪，以及足够的智能来将数据融合为实际位置数据。

该项目应该易于复制。它由现成的模块、分线板和常见组件(如电池、开关和一些磁铁)组成。还有一个 3D 打印的外壳来掩盖这一切。

当然，另一个答案是将[做成夹具](https://hackaday.com/2016/09/23/home-made-adjustable-knife-jig/)以合适的角度拿刀。如果你不喜欢手工磨刀，[我们也可以帮](https://hackaday.com/2015/03/18/sharpening-knives-using-a-bread-slicer/)一把。

 [https://www.youtube.com/embed/hqzrYcssgiI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hqzrYcssgiI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


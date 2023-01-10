# 精心设计的升压转换器通过 USB 充电器为 Nixies 供电

> 原文：<https://hackaday.com/2018/03/12/nicely-engineered-boost-converter-powers-nixies-from-usb-charger/>

爱他们或恨他们，日本人会留下来。它们持久的吸引力在很大程度上是因为它们很难即插即用；产生驱动复古显示器所需的高压是它们魅力的一部分。但大多数谢妮电源似乎希望输入端为 9 伏或更高，这使得将它们集成到典型的 USB 供电的微控制器项目中变得困难。

解决这个问题是[马克·史密斯]5 伏谢妮电源背后的想法。总体目标很简单:5 伏输入，170 伏输出，20 毫安。但是[Mark]特别注意通过精心设计将升压转换器的 EMI 输出降至最低，他设法将所有东西都装入一个紧凑的 14 厘米 PCB 中。他在[对他的初始设计进行了大量仔细的实验](https://surfncircuits.com/2018/02/03/optimizing-the-5v-to-170v-nixie-tube-power-supply-design-part-2/)，以验证他已经达到了设计目标，然后在[开始了 KiCad](https://surfncircuits.com/2018/03/03/kicad-power-tools-help-shrink-the-nixie-tube-power-supply-part-3/) 中的一个小调整任务，将 PCB 的尺寸减少了 27%。这三篇独立的博客文章非常值得任何有兴趣了解电子设计的人阅读。

现在[马克]有了他的谢妮电力供应，它会变成什么样？我们不能肯定地说，但它将是一个时钟。它总是[一个时钟](http://hackaday.com/2017/01/17/sculptural-nixie-clock-has-shockingly-exposed-design/)。除非是[功率表](http://hackaday.com/2016/01/10/nixie-tubes-adorn-steampunk-solar-power-meter/)或者[速度计](http://hackaday.com/2015/07/16/nixie-tube-speedometer-in-motorcycle-handlebars/)。
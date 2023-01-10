# 蒸汽朋克风格的艺术钟！

> 原文：<https://hackaday.com/2017/07/04/steampunk-inspired-art-clock/>

做你喜欢的事情并获得报酬是一种特殊的享受。一个机械师和制造者——业余爱好者黑客——[ spdltd]被委托建造一个带有蒸汽朋克风格的机械艺术装置。有了完全的创造性控制，他说服了他的客户让他做一些有用的东西:一个巨大的电动机械钟。

这个古怪的设计由铜、黄铜、钢、铝和不锈钢拼凑而成，使用 Arduino Yun(Linux 和 Arduino 微控制器板的组合)来控制步进电机并在互联网上查询当地时间。启动后，时钟自动校准，通过旋转钟面，直到一个传感器检测到一个额外的 peg，并使用该零在 12 点钟；然后，Yun 通过 WiFi 获取当地时间，并向步进电机发送“a-spinning ”,直到显示正确的时间。

乍一看，你可能会发现很难准确读出现在是什么时间，但一旦它与每小时上方的凹槽对齐，重点作品的钉就表示一刻钟。至少这个不需要你[配色或者做很多数学运算](http://hackaday.com/2017/05/05/4-led-octal-clock-demands-colorful-math/)来检查时间。

 [https://www.youtube.com/embed/mMqp_Zk1CwU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mMqp_Zk1CwU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



将来[spdltd]更愿意花更多的时间在构建的软件部分上，以确保其完整性，也许还会加入一些特殊的东西，以便在时钟报时时时发生。
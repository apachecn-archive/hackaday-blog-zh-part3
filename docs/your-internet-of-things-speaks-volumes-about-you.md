# 你的物联网充分说明了你

> 原文：<https://hackaday.com/2017/02/26/your-internet-of-things-speaks-volumes-about-you/>

要是马尔夫和哈里今天是窃贼就好了；他们可能会发现，通过利用[Luc Volders]在 ThingSpeak 上注意到的潜在漏洞,对房屋进行分类会容易得多，而且——也许——会知道哪些房屋被倾向于技术的孩子占据了。

作为一项物联网服务，ThingSpeak 从 ESP-8266 中获取数据，绘制图表，并公开显示数据。你们中的一些人可能已经看到了这个趋势。当[Volders]使用这项服务进行测试时，他意识到任何人都可以检查他的人洞穴的温度——从而推断出房子何时空置，因为位置数据碰巧也是公开的。稍微调查一下，就发现了其他几个有温度数据的频道，或者与某个位置相关联的频道，那些心怀不轨的人可能会滥用这些频道。

这不是软件本身的漏洞，但[Volders]很好地观察到，每当你使用在线物联网服务时，隐私设置必须需要改变。尽管物联网互联令人惊叹，但始终要[意识到不利因素](http://hackaday.com/2015/10/08/get-your-internet-out-of-my-things/)并采取措施[减轻它们](http://hackaday.com/2015/10/08/get-your-internet-out-of-my-things/)。
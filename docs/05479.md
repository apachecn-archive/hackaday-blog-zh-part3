# 俄罗斯黑客领域前沿

> 原文：<https://hackaday.com/2017/03/28/russian-hackers-domain-fronting/>

火眼刚刚发布了一份报告，称发现俄罗斯黑客组织“高级持续威胁 29”(apt 29，因为缺乏更好的代号)[利用 TOR 的`meek`插件隐藏他们的流量](https://www.fireeye.com/blog/threat-research/2017/03/apt29_domain_frontin.html)。如果你在 meek-reflect.appspot.com 上使用`meek`，你会发现它已经被关闭了。如果所有这些对你来说都是胡言乱语，请继续往下读。

[`meek`](https://trac.torproject.org/projects/tor/wiki/doc/AChildsGardenOfPluggableTransports#meek) 是一款聪明的软件。想象一下，你想和 [Tor 匿名网络](https://trac.torproject.org/projects/tor)交流，但是你不想让任何人知道你在交流。也许你生活在一个国家，那里的防火墙阻止你访问整个网络，并阻止 Tor 入口节点作为他们伟大防火墙的一部分。为了自由交流，你会想先把流量发送到无关紧要的地方，然后再把它发送到 Tor。

这就是`meek`所做的，但它更进一步。reflector 服务器使用与流行服务相同的内容交付网络(CDN)托管，比如谷歌的搜索引擎。CDN 有一个 IP 地址，就像互联网上的每一台计算机一样，但它为它托管的各种服务提供内容。到 CDN 的流量，用 TLS 加密，无论是去`meek`反射器还是去谷歌，看起来都是一样的，所以外面没人能知道这是搜索查询还是去往 tor 的数据包。在 CDN 内部，它是未加密的，并被传递给反射器。

总之，`meek`的发明是为了帮助生活在暴虐政权下的人们接触未经审查的互联网，现在网络安全研究人员观察到它被俄罗斯国家黑客用来隐藏他们的踪迹。叹气。技术不知道自己站在哪一边——联邦调查局想在我们所有的通信中植入的后门也很容易被黑手党利用。旨在给人们带来言论自由的插件很容易被用来隐藏民族国家黑客的行动。

我们生活在一个多么奇怪的世界。
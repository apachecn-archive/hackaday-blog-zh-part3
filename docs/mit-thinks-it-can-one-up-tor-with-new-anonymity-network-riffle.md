# 麻省理工学院认为它可以在新的匿名网络 Riffle 上领先 TOR

> 原文：<https://hackaday.com/2016/07/12/mit-thinks-it-can-one-up-tor-with-new-anonymity-network-riffle/>

Tor 是匿名网络中家喻户晓的名字，但是这个系统存在漏洞，特别是当攻击者发现谁在发送和接收信息时。麻省理工学院和洛桑联邦理工学院的研究人员认为，他们在一个名为 Riffle 的系统中找到了一种更好的方法。你可以[钻研白皮书](http://people.csail.mit.edu/devadas/pubs/riffle.pdf)，但是麻省理工学院的新闻文章[在提供概述方面做得很好](http://news.mit.edu/2016/stay-anonymous-online-0711)。

Tor 的核心优势是组成网络名称最后两个字母的[洋葱路由](https://en.wikipedia.org/wiki/Onion_routing)。Riffle 保留了这一方面，并以一种新颖的方式建立在它的基础上。洋葱类比与皮肤层有关——发送计算机对信息进行多次加密，当信息通过每个服务器时，一层加密被移除。

Riffle 首先向网络中的每一台服务器发送消息。然后，它使用[混合网络](https://en.wikipedia.org/wiki/Mix_network)以不可预测的方式将消息路由到最终目的地。只要网络中至少有一个服务器未被破坏，在验证初始消息时(或通过随后的[认证加密](https://en.wikipedia.org/wiki/Authenticated_encryption)检查，当消息通过每个服务器时)，篡改将被发现。

混合网络与消息验证的结合是这里的新颖之处。由于使用了加密技术，这条信息已经是安全的了，但是 Riffle 也将保护发送者和接收者的匿名性。

[via [Engadget](https://www.engadget.com/2016/07/11/mit-anonymity-network-more-secure-than-tor/)
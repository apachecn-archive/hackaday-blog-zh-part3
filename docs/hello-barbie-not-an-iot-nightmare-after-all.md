# “你好芭比”毕竟不是什么噩梦

> 原文：<https://hackaday.com/2016/01/29/hello-barbie-not-an-iot-nightmare-after-all/>

安全研究人员可能是一群冷酷的人。当仔细观察时，一切都在某种程度上是不安全的，这导致了业内的许多悲观情绪。因此，看到一份既不悲观也不悲观的安全报告让人有点震惊。

我们之前报道过 Somerset Recon 对“Hello Barbie”的最初拆解，并屏息等待固件转储和一些真正的逆向工程。嗯，它发生了[基本上一切看起来都很好(PDF 报告)](http://somersetrecon.com/s/HelloBarbieSecurityAnalysis.pdf)。萨默塞特的人拆下了芯片，扔掉了闪存 ROM，当 [IDA-dust](https://www.hex-rays.com/products/ida/index.shtml) 尘埃落定时，美泰使用了类似于其他人用来运行亚马逊云服务代理的固件，但目标是“toytalk.com”网络。简而言之，它使用一个经过测试的基本上可靠的固件。

令人毛骨悚然的说话娃娃连接的网络服务是另一个故事，充满了漏洞，在整个萨默塞特的调查中正在积极修补，但我们只对固件感兴趣，这看起来没问题。在物联网安全领域，并非一切都是恐怖故事。有些故事*做*有一个美好的结局。芭比今晚可以睡个好觉了。
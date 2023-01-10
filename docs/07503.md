# DUHK:不要使用硬编码的键

> 原文：<https://hackaday.com/2017/10/25/duhk-dont-use-hard-coded-keys/>

标题读起来就像密码学 101 或密码俱乐部第一条规则的讲座名称。事实上，DUHK 并不是这两者中的任何一个，而是最近披露的伪随机数生成算法(PNRG)中的一个漏洞的名称，该算法直到最近还是联邦标准 X9.31 的一部分。

随机数对于可行的加密技术至关重要。它们也很难获得解决方案，比如利用由量子效应控制的[半导体](https://hackaday.com/2014/06/08/the-development-of-a-hardware-random-number-generator/)或[衰变物质](https://hackaday.com/2015/08/16/hackaday-prize-entry-nuclear-powered-random-number-generator/)的物理特性。下一个最好的解决方案是记录难以预测的事件，比如敲击键盘的[计时](https://en.wikipedia.org/wiki/Entropy_(computing)#Linux_kernel)。随机性最弱的来源是数学，这是有道理的，因为数学最受欢迎的特征之一是它的可预测性。数学解决方案有一个可取之处，那就是能够在短时间内产生大量对人类来说看起来随机的数字。

PNRGs 需要一个开始产生输出的起点。一旦知道了这个种子，产生的序列就变得可预测了。

X9.31 PNRG 是一种用于各种加密算法的算法，几十年来一直在[联邦信息处理标准](https://en.wikipedia.org/wiki/Federal_Information_Processing_Standards)中获得认证，直到 2016 年从批准的标准列表中删除。DUHK 背后的研究人员发现，该标准允许种子存储在其实现的源代码中。下一步是寻找能做到这一点的软件，他们在运行于 VPN 网关上的旧版本 [FortiOS](https://www.fortinet.com/products/fortigate/fortios.html) 中发现了 X9.31。

### 我应该担心吗？

可能是，也可能不是。DUHK 背后的团队发表的分析( [PDF](https://duhkattack.com/paper.pdf) )指出，该漏洞仅限于传统实现，不允许接管运行它们的设备，只能窃听“安全”连接。这种攻击的范围比通过[蓝牙](https://hackaday.com/2017/09/14/bluetooth-vulnerability-affects-all-major-os/)远程执行代码的攻击要小得多。另一方面，这也为严格审查标准和技术认证提供了有力的证据。该团队的行为也让我们深入了解了这里经常讨论的白帽黑客的最佳实践。他们有一首很棒的[主题曲](https://www.youtube.com/watch?v=bf9d7rSf_Ks)。
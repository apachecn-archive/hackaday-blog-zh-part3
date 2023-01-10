# ASLR^CACHE 攻击挫败地址空间布局随机化

> 原文：<https://hackaday.com/2017/02/15/aslrcache-attack-defeats-address-space-layout-randomization/>

来自 VUSec 的研究人员发现了一种通过 [MMU 旁道攻击](https://www.vusec.net/projects/anc/)破解 ASLR 的方法，这种方法甚至在 JavaScript 中也有效。这重要吗？是的，有关系。很多。这个安全缺陷的发现以及实际的实现非常重要，主要是因为两个因素:ASLR 被破解意味着什么，以及 MMU 侧信道攻击在处理器内部是如何工作的。

地址空间布局随机化或 ASLR 是一种重要的防御机制，可以减少已知的安全缺陷，更重要的是，可以减少未知的安全缺陷。顾名思义，ASLR 通过在主程序启动时随机化进程地址，使恶意程序更难危害系统。这意味着它不太可能可靠地跳转到内存中某个被利用的特定函数或攻击者植入的某段外壳代码。

破解 ASLR 是简化漏洞利用并使其更加可靠的一大步。能够在 JavaScript 中实现这一点意味着使用这种技术的漏洞可以击败运行 JavaScript 的 web 浏览器 ASLR 保护，这是互联网用户最常见的配置。

ASLR 以前在某些特定场景下被攻破过，但这次新的攻击凸显了一个更深刻的问题。由于它利用了现代处理器的内存管理单元(MMU)使用处理器的高速缓存层次结构来提高页表遍历的性能，这意味着缺陷存在于硬件本身，而不是正在运行的软件。软件供应商可以采取一些措施来缓解这一问题，但全面和适当的修复将意味着更换或升级硬件本身。

在他们的论文中，研究人员得出了一个戏剧性的结论:

> “……结论是，这种缓存行为和强地址空间随机化是相互排斥的。由于缓存层次结构对整体系统性能的重要性，所有的修复都可能成本过高而不切实际。此外，即使缓解措施在硬件中是可能的，比如为页表提供单独的缓存，这些问题也可能在软件中再次出现。因此，我们建议不要再将 ASLR 作为防御内存错误攻击的第一道防线，未来的防御也不要依赖它作为关键的构建模块。”

所有细节可以参考[课题组的论文](http://www.cs.vu.nl/~herbertb/download/papers/anc_ndss17.pdf)。同时，他们给我们留下了一些演示攻击 ASLR 的视频。最快的一次只用了 25 秒:

 [https://www.youtube.com/embed/aILISvZlBAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aILISvZlBAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


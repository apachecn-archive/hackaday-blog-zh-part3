# Shmoocon 2016:后量子世界中的计算

> 原文：<https://hackaday.com/2016/01/16/shmoocon-2016-computing-in-a-post-quantum-world/>

密码专家说，没有什么比量子计算更危险的了。量子计算机不是像传统计算机那样使用晶体管的状态来保存一位的值，而是使用量子位，或者像光子偏振一样的量子信息。按照对量子计算机一无所知的人的说法，它们是末日的开始，是所有密码学的打破，是机器的崛起。幸运的是，[Jean-Philippe Aumasson]实际上对量子计算机略知一二，并能够在他本周末的 Shmoocon 演讲“加密、量子和后量子”中教给我们一些东西

这个演讲是[Jean-Philippe]的 DEF CON 23 [演讲的延续，该演讲涵盖了量子计算的基础知识](https://media.defcon.org/DEF%20CON%2023/DEF%20CON%2023%20presentations/DEFCON-23-Phillip-Aumasson-Quantum-Computers-vs-Computers-Security.pdf) (PDF)简而言之，量子计算机并不快——它们只是非常非常专业的算法的协处理器。量子计算机没说 P=NP，反正也不能用在 NP 难的问题上。量子计算机唯一具有的优势是完全摧毁公钥密码系统的能力。任何使用 RSA，Diffie-Hellman，椭圆曲线的加密形式都是完全彻底的被破解了。有了量子计算机，我们就完了。这没关系，根据 DEF CON talk——真正的量子计算机可能永远也不会建成。

敏锐的读者会质疑量子计算机可能永远不会被制造出来的事实。毕竟， [D-Wave 正在向谷歌、洛克希德和美国宇航局出售量子计算机](http://www.dwavesys.com/quantum-computing)。这些不是真正的量子计算机。即使它们比个人电脑快 [1 亿倍，它们也只是在一个非常特殊的算法上更快。这些计算机无法模拟通用量子计算机。他们不能执行 Shor 算法，一种寻找整数的质因数的算法。它们不可扩展，不具备容错能力，也不是通用量子计算机。](http://www.telegraph.co.uk/technology/news/12042781/Google-D-Wave-quantum-computer-is-100-million-times-faster-than-your-PC.html)

就真正的量子计算机而言，已经制造出来的最大的计算机只包含少量的量子位。要破解 RSA 和其他加密技术，需要数百万个量子位。有些算法需要量子 RAM，没人知道怎么构建。那么为什么量子计算如此可怕呢？如果量子计算机存在，RSA，ECC，Diffie-Hellman，PGP，SSH，比特币都会在一夜之间消亡。对于劫持你的无人驾驶汽车或把智能联网恒温器的显示从华氏温度改为摄氏温度的人来说，这是一个可怕得多的提议。

对量子计算机的定论是什么？不太好，如果你问[让-菲利普]。在他看来，100 年后我们才会有量子计算机。在那之前，crypto 是安全的，如果你使用足够长的密钥，NSA 不会破解你的 codez。
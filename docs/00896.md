# 用 Spritz 加密 Arduino

> 原文：<https://hackaday.com/2015/12/12/encryption-for-arduino-with-spritz/>

Hackaday.io 用户[Abderraouf]已经为 Arduino 编写了新的(ish) Spritz 密码和散列的[实现。虽然我们还没有大到足以评估代码安全性的程度，但看起来它会非常方便。](https://hackaday.io/project/8244-arduino-spritz-cipher-library)

Spritz 本身就是一个简洁的密码。它不是接收固定的数据块并对其进行操作，而是允许您(几乎)以自然的方式处理它，然后分段提取加密的结果。它既可用作双向密码，也可用作单向哈希函数。看起来 Spritz 是满足您所有加密需求的一站式商店，现在您可以在 Arduino 上运行它。

如果你害怕新密码的新实现(你*应该*害怕)，Spritz 的血统应该有助于让你放松:它是由[ [罗恩·里维斯](https://en.wikipedia.org/wiki/Ron_Rivest)开发的，是他的 RC4 算法的继任者，它融合了过去关于该算法的许多经验教训。这并不排除库实现中的细微缺陷(无意冒犯，[Abderraouf]！)或您的下游工作，但至少底层算法似乎是真实的交易。

[Abderraouf]在他的文章中链接了它，但为了完整起见，这里有 [Spritz 论文(PDF)](https://people.csail.mit.edu/rivest/pubs/RS14.pdf) 。您目前在 Arduino 或微控制器项目中使用哪些加密库？我们已经是 [XXTEA](https://en.wikipedia.org/wiki/XXTEA) 的粉丝很久了，但更多的是因为它简单小巧，而不是因为它安全。Spritz 可能足够简单，易于实现，而且更加安全。太好了。
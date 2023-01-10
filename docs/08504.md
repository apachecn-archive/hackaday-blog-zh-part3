# 这个 NES 光盘是其源代码的压缩文件

> 原文：<https://hackaday.com/2018/02/06/this-nes-rom-is-a-zip-of-its-source/>

用计算术语来说，多语是具有多种有效含义的文件。我们在[《国际政治经济学杂志||GTFO](https://hackaday.com/2017/08/14/bibles-you-should-read-poc-gtfo/) 》中看到了一些令人惊叹的多语言文件的例子。一个例子:一个 PDF，也是一个 ZIP、HTML 文件和 BPG 图像。

[Vi Grey]的灵感来自于 PoC||GTFO 为[期 0x14](https://www.alchemistowl.org/pocorgtfo/pocorgtfo14.pdf) 发布的 PDF/ZIP/NES ROM 混合文件。使用[不同的方法](https://vigrey.com/blog/this-nes-rom-also-zip-file)，【Vi】创建了一个文件，它既是 NES ROM 又是 ZIP，其中 ZIP 的全部内容都存储在 NES ROM 中。

当 PoC||GTFO 创造了他们的 NES ROM 多语言版本时，他们把大部分信息粘在了 NES ROM 的边界之外。虽然文件是有效的，但如果它被刻录到一个磁带上，您将会丢失 ZIP 存档。

[Vi]的多语不同。从一个真正的 NES 墨盒上撕下来，你会得到一个 ZIP 文件。解压后，你就可以得到源代码了。编译源代码，您会得到一个包含源代码的有效 ZIP 文件。把它烧成一个盒子，然后…希望你在这一点上找到了递归。

Github 上有将多种语言混合在一起的源代码和脚本[。](https://github.com/ViGrey/neszip-example)
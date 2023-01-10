# 从芯片中提取密码

> 原文：<https://hackaday.com/2017/10/30/pull-passwords-out-of-silicon/>

[q3k]在正在进行的 Pwn2Win capture-the-flag 中得到了一个非常酷的问题，他通过对 VLSI IC 中编码密码的金属互连层进行解码[彻底解决了这个问题。他不是租用别人的网表提取代码，而是通过](http://blog.dragonsector.pl/2017/10/pwn2win-2017-shift-register.html)[编写自己的](https://github.com/q3k/ctf/tree/master/Pwn2Win2017)来完成的。

Pwn2Win CTF 的问题出现在一个假想的火箭发射代码的设计文件中。定制 IC 接受一个 ASCII 字符串作为输入，如果匹配，将引脚翻转为高电平。在逻辑上，最简单的方法可能是实现一个足够长的移位寄存器来存放代码串的位，然后硬连线一些组合逻辑，只有当所有位都正确时，组合逻辑才会读取 true。

(不，你不希望以这种方式实现密码检查器——这意味着你可以非常容易地简单地暴力破解密码——但是[这样的实现已经被广泛使用](https://hackaday.com/2015/06/08/hacking-the-im-me-to-open-garages/)。)

总之，回到我们的故事。在反转网表之后，[q3k]在一个链中定位了 320 个触发器，暗示了一个 40 字节的 ASCII 代码串。在从“解锁”引脚到触发器的电路中反向工作，他发现了一个 NOR 和 NAND 门的网络，这些门被转换成逻辑符号，然后被扔进 [Z3](https://github.com/Z3Prover/z3) 中求解。几个周期后，他直接从硅片中取出了密码！

如果你对逻辑设计或硬件逆向工程感兴趣，这看起来是一个非常有趣的挑战。当然，你不必编写自己的工具来做到这一点，但是[q3k]会说这是值得的。

感谢[Victor]的精彩提示！由[大卫·卡伦](https://en.wikipedia.org/wiki/Standard_cell#/media/File:Eda-fabrication.PNG)通过维基百科提供的特色图片。
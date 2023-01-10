# 傻傻的十六进制文件

> 原文：<https://hackaday.com/2016/07/13/gawking-hex-files/>

上次我谈到了如何使用 AWK(或者更有可能是 GNU AWK GAWK)来处理文本文件。你可能会想:我为什么要在乎？硬件黑客不需要文本文件吧？也许他们有。我想谈谈一些常见的情况，在这些情况下，AWK 可以处理更适合硬件黑客的东西。

## 简单:数据日志

如果你环顾四周，许多数据记录器和测试仪器*确实*产生文本文件。如果你有一个来自你的作用域的文本文件或者一个像 [SIGROK](https://hackaday.com/2016/04/02/hack-your-multimeter/) 这样的程序，用 AWK 对它进行分割是很简单的。你的机器可能不会总是输出格式良好的文本文件。这就是 AWK 的意义所在。

AWK 作出了默认的假设，即字段在空格处断开，并以换行符结束。然而，你可以用很多方法改变这些假设。您可以设置`FS`和`RS`分别改变字段分隔符和记录分隔符。通常，你可以在`BEGIN`动作中设置它，尽管你也可以在命令行中改变它。

例如，假设您的测试文件在字段之间使用分号。没问题。只需将`FS`设置为“；”你已经准备好了。将`FS`设置为一个新行会将整行视为一个单独的字段。除了分隔字段，您还可能遇到固定宽度的字段。对于这样的文件，你可以设置`FIELDWIDTHS`。

如果记录不是分隔的，而是固定长度的，事情就有点棘手了。有些人使用 Linux 实用程序 [dd](http://linux.die.net/man/1/dd) 根据每个记录的字节数将文件分成几行。您也可以将 [`RS`设置为有限数量的任意字符，然后使用`RT`变量](https://www.gnu.org/software/gawk/manual/gawk.html#gawk-split-records)(见下文)找出这些字符是什么。还有其他选择，甚至是读取多行的方法。如果你有这些情况，那么 [GAWK 手册](https://www.gnu.org/software/gawk/manual/gawk.html#Reading-Files)就是你的朋友。

```
BEGIN { RS=".{10}"   # records are 10 characters
      }

   {
   $0=RT
   }

   {
   print $0  # do what you want here
   }
```

一旦对记录和字段进行了排序，就很容易计算平均值、检测超出限制的值，以及您能想到的任何其他事情。

## 电子表格数据日志

一些工具输出电子表格。AWK 不擅长直接处理电子表格。然而，电子表格可以保存为 CSV 文件，然后 AWK 可以很容易地咀嚼它们。这也是一种从 AWK 文件生成的简单格式，然后可以读入电子表格。如果您不想使用 [GNUPlot](http://www.gnuplot.info/) ，那么您可以轻松地制作出漂亮的图形。

简单地说，将`FS`设置为逗号就可以了。如果你只有数字，这可能就足够了。但是，如果有字符串，一些程序会在字符串两边加上引号(可能包含逗号或空格)。有些只在有逗号的字符串上加引号。

为了彻底解决这个问题，AWK 提供了另一种定义字段的方法。通常，`FS`会告诉你用什么字符来分隔一个字段。但是，您可以设置`FPAT`来定义字段的外观。在 CSV 文件的情况下，字段是除逗号或双引号之外的任何字符，然后是下一个双引号之前的任何字符。

手册中有[一个很好的例子](https://www.gnu.org/software/gawk/manual/html_node/Splitting-By-Content.html#Splitting-By-Content):

```
BEGIN {
  FPAT = "([^,]+)|(\"[^\"]+\")"
  }

  {
  print "NF = ", NF
  for (i = 1; i <= NF; i++) {
  printf("$%d = <%s>\n", i, $i)
  }
```

这并不完美。例如，转义引号不能正常工作。带新行的引用文本也不会。手册做了一些修改，删除了引号并处理了空字段，但是上面的例子适用于大多数常见的情况。通常最简单的方法是将源程序中的分隔符改为唯一的，而不是逗号。

## 十六进制文件

硬件界常见的另一个文本文件是十六进制文件。这是一个文本文件，表示可编程存储器(可能嵌入在微控制器中)的十六进制内容。有两种常见的格式:英特尔十六进制文件和摩托罗拉的记录。AWK 可以处理这两个，但我们将重点放在英特尔变种。

旧版本的 AWK 不能很好地处理十六进制输入，所以你不得不求助于构建数组来将十六进制数字转换成数字。有时在旧代码或力求兼容的代码中，你仍然会看到这种情况。然而，GNU AWK 有一个`strtonum`函数，它可以显式地将一个字符串转换成一个数字，并且理解 0x 前缀。所以一个高度兼容的两位十六进制函数看起来像这样(不包括初始化`hexdigit`数组的代码):

```
function hex2dec(x) {
  return (hexdigit[substr(x,1,1)]*16)+hexdigit[substr(x,2,1)]
}
```

如果您不介意要求 GAWK，它可能看起来像这样:

```
function hex2dec(x) {
  return strtonum("0x" x);
}
```

事实上，最后一个函数稍微好一点(但命名有误),因为它可以处理任何十六进制数，而不管长度如何(达到 GAWK 中的任何限制)。

十六进制输出很简单，因为有了`printf`和 X 格式说明符。下面是一个 AWK 脚本，它仔细检查了一个十六进制文件，并提供了整个文件的计数，还显示了段的细分(即非连续内存区域)。

```
BEGIN { ct=0;
  adxpt=""
}

function hex4dec(y) {
  return strtonum("0x" y)
}

function hex2dec(x) {
  return strtonum("0x" x);
}

/:[[:xdigit:]][[:xdigit:]][[:xdigit:]][[:xdigit:]][[:xdigit:]][[:xdigit:]]00/ {

  ad = hex4dec(substr($0, 4, 4))
  if (ad != adxpt) {
  block[++n] = ad
  adxpt = ad;
    }
  l = hex2dec(substr($0, 2, 2))
  blockct[n] = blockct[n] + l
  adxpt = adxpt + l
  ct = ct + l
  }

END { printf("Count=%d (0x%04x) bytes\t%d (0x%04x) words\n\n", ct, ct, ct/2, ct/2)
  for (i = 1 ; i <= n ; i++) {
  printf("%04x: %d (0x%x) bytes\t", block[i], blockct[i], blockct[i])
  printf("%d (0x%x) words\n", blockct[i]/2, blockct[i]/2)
  }

}
```

这展示了一些 AWK 的特性:`BEGIN`动作、用户定义的函数、命名字符类的使用(`:xdigit:`是一个十六进制数字)和数组(`block`和`blockct`使用数字索引，尽管它们不是必须的)。在`END`动作中，摘要使用`printf`语句进行十进制和十六进制输出。

一旦可以解析这样的文件，就可以对结果数据做很多事情。这里有一个类似代码的[例子，它对十六进制文件](https://gist.github.com/houmei/3860208)进行健全性检查。

## 二进制文件

文本文件很好，但是真正的硬件使用二进制文件，人们(和 AWK)不容易阅读，对不对？嗯，也许是人，但 AWK 可以用几种方式读取二进制文件。您可以在脚本的开始部分使用`getline`,并控制如何直接读取内容。您还可以使用上面提到的 RS/RT 技巧来读取特定数量的字节。如果你感兴趣的话，你可以看看其他一些只适用于 AWK 的方法。

然而，在 AWK 处理二进制文件最简单的方法是使用类似 od 实用程序的工具将它们转换成文本文件。这是一个可用于 Linux(或 Cygwin，可能还有其他 Windows 工具包)的程序，它将二进制文件转换成不同的可读格式。您可能需要十六进制字节，所以这是-t x2 选项(或者使用 x4 表示 16 位字)。但是，输出是为人类而不是机器生成的，所以当出现长时间的相同输出时，od 会省略它们，用一个星号替换所有缺少的行。对于 AWK 使用，您希望使用-v 选项来关闭该行为。还有其他选项可以改变地址的输出基数、交换字节等。

下面是随机二进制文件中的几行:

```
0000000 d8ff e0ff 1000 464a 4649 0100 0001 0100
0000020 0100 0000 dbff 4300 5900 433d 434e 5938
0000040 484e 644e 595e 8569 90de 7a85 857a c2ff
0000060 a1cd ffde ffff ffff ffff ffff ffff ffff
0000100 ffff ffff ffff ffff ffff ffff ffff ffff
0000120 ffff ffff ffff ffff ffff 00db 0143 645e
0000140 8564 8575 90ff ff90 ffff ffff ffff ffff
0000160 ffff ffff ffff ffff ffff ffff ffff ffff
0000200 ffff ffff ffff ffff ffff ffff ffff ffff
0000220 ffff ffff ffff ffff ffff ffff ffff c0ff
0000240 1100 0108 02e0 0380 2201 0200 0111 1103
0000260 ff01 00c4 001f 0100 0105 0101 0101 0001
0000300 0000 0000 0000 0100 0302 0504 0706 0908
0000320 0b0a c4ff b500 0010 0102 0303 0402 0503
0000340 0405 0004 0100 017d 0302 0400 0511 2112
0000360 4131 1306 6151 2207 1471 8132 a191 2308
```

用 AWK 解析这个非常简单。地址将是`$1`，每个字段将是`$2`、`$3`等。您可以自己转换文件，在 shell 中使用管道，或者——如果您想要一个干净的解决方案——让 AWK 作为[子流程](https://www.gnu.org/software/gawk/manual/gawk.html#Getline_002fPipe)运行 od。因为输入是文本，所以 AWK 的所有正则表达式特性仍然有效，这很有用。

编写二进制文件也很容易，因为`printf`几乎可以输出任何内容。另一种方法是用 xxd 代替 od。它可以将二进制文件转换成文本，也可以反过来。

## 全语言

有句老话说，如果你只有一把锤子，那么所有的东西看起来都像钉子。我怀疑 AWK 是构建完整语言的最佳工具，但它可能是一些快速和肮脏的黑客的组成部分。例如，[通用交叉汇编程序](https://hackaday.com/2015/08/06/hacking-a-universal-assembler/)使用 AWK 将汇编语言文件转换成 C 预处理器可以处理的内部格式

由于 AWK 可以很容易地调用外部程序，因此有可能编写一些东西，例如，处理命令的文本文件，并用它们来驱动机器人手臂。正则表达式匹配使文本处理变得容易，外部程序实际上可以处理硬件接口。

[![awk-wolfenstein](img/703d3d1129b1408620c8f66444c8ed16.png)](https://hackaday.com/wp-content/uploads/2016/06/awk-wolfenstein.png) 觉得那很牵强？我们已经讨论了更奇怪的 AWK 用例，包括一个类似 [Wolfenstien 的游戏](https://hackaday.com/2016/01/15/wolfenstein-in-600-lines-of-code/)，它使用了 600 行 AWK 脚本(如右图所示)。

所以，它肯定是软件，但它是一个具有瑞士军刀品质的工具，使它成为软件和硬件黑客的有用工具。当然，其他工具如 Perl、Python，甚至 C 或 C++可以做得更多。但是通常要付出复杂性和学习曲线的代价。AWK 并不适合每一份工作，但是当它起作用时，它就很有效。
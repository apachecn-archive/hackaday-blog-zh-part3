# Shell 脚本程序的 Lint

> 原文：<https://hackaday.com/2017/03/29/lint-for-shell-scripters/>

过去，编写嵌入式软件的乐趣之一就是永远不必部署 shell 脚本。但是现在，随着像 Raspberry Pi 这样的平台变得非常普遍，Linux shell 脚本可以成为系统的一大部分——在某些情况下甚至是整个系统。在部署之前，您如何知道您的 shell 脚本没有错误呢？当然，没有什么可以捕捉所有的错误，但是你可以试试 [ShellCheck](https://www.shellcheck.net/) 。

当你编译一个 C 程序时，编译器通常会捕捉到你的大部分错误。但是，shell 在运行之前不会查看所有内容，这意味着您可能会在等待 if 语句的正确路径或错误的文件名时出错。ShellCheck 可以帮助您在部署之前识别这些问题。

如果你不喜欢将你的脚本粘贴到网页中，你可以通过访问 [GitHub](https://github.com/koalaman/shellcheck) 在本地安装 checker。那里的 readme 文件也解释了该工具可以捕获什么样的东西。它甚至可以与常见的编辑器集成(如下面的视频所示)。

例如，shell 脚本的一个常见问题是忘记引用一个环境变量，该变量可能包含一个包含空格的文件名。例如，考虑这个非常简单的脚本:

```
#!/bin/bash
echo Processing $1
cat $1 >$2
```

只要文件名称中没有空格，这样做就可以了。但是，假设输入文件的名称是“Hack A Day.txt”，那么您会得到:

```
$ ./bad "Hack A Day.txt" hello
Processing Hack A Day.txt
cat: Hack: No such file or directory
cat: A: No such file or directory
cat: Day.txt: No such file or directory
```

1 美元扩展为三个词:Hack、A 和 Day.txt。对于 echo 来说，这不是问题。它只是打印它们。但是最后一行变成了:

```
cat Hack A Day.txt >hello
```

这是行不通的(除非有三个同名文件，否则它将无法正常工作)。当然，答案是在 cat 行上加上大约 1 美元(或者 2 美元)的报价。在回声线上也不会痛。

ShellCheck 将会发现这类问题以及更多问题。例如，下面是一个更加雄心勃勃的脚本的部分输出:

```
Line 5:
if [ "$0" == "$BASH_SOURCE" ]
^-- SC2128: Expanding an array without an index only gives the first element.

Line 8:
echo E.g.: . $0
^-- SC2086: Double quote to prevent globbing and word splitting.

Line 15:
alias pathed=". $BASH_SOURCE"
^-- SC2128: Expanding an array without an index only gives the first element.
^-- SC2139: This expands when defined, not when used. Consider escaping.

Line 29:
if [ "$PATHEDIT_OLD" = "$PATHEDIT_NEW" -o ! -s "$PATHEDIT_FN" ]
^-- SC2166: Prefer [ p ] || [ q ] as [ p -o q ] is not well defined.
```

像任何类似的工具一样，您必须解释结果。例如，第 8 行中的 echo 语句并不真正关心$0 是否有引号，但是该工具无法判断出这一点。

ShellCheck 会捕捉到所有内容吗？不会。但是它会捕捉到您在部署一个 shell 脚本后很长一段时间内可能找不到的东西。

如果你认为你不能在 bash 脚本中做很多事情，那么[再考虑一下](https://hackaday.com/2013/02/05/bash-games/)。如果这对你来说不够实际，可以考虑用[从网页上抓取数据](https://hackaday.com/2010/12/25/crash-course-in-html-manipulation-from-a-shell-script/)作为例子。

 [https://www.youtube.com/embed/t4FP7tHXtEU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t4FP7tHXtEU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


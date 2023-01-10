# 编辑战争:维姆的复仇

> 原文：<https://hackaday.com/2016/08/08/editor-wars-the-revenge-of-vim/>

我很少在这几页上读到如此无聊的文章！Al Williams 对 Emacs 和 Vim 的报道是对我们普通读者应得的深度报道的冒犯。在试图做到“不偏不倚”的同时，他用七句话总结了终极编辑 Vim。七句话！蒸汽像燥山姆一样从我的耳朵里涌出来。

T2 艾尔，像你们中的许多人一样，认为他“知道如何使用 vi”。我在这里告诉你，他没有。除非你在过去几年里独自一人呆在喜马拉雅山的一个山洞里，只有食物、饮料、笔记本电脑和 [Vim 高尔夫](http://vimgolf.com/)，否则你可能也不会。见鬼，我不认为自己是 Vim 大师，但我要写这篇过度紧张的文章来称赞它(自然是使用 Vim)。

我写这篇文章的原因不是为了延续 vi 对 Emacs 的战争。无论如何，这个想法是愚蠢的，可能是 Emacs 的人发明的，用来抢 vi 的风头。你看，vi 对 Emacs 是在转移注意力。Vi 和 Vim 如此奇怪，与你可能使用的任何其他编辑器如此不同，以至于相比之下，它使 Emacs 看起来简单乏味:它只是一个具有体面可扩展性的普通编辑器(如果你能忍受 Lisp)，可怕的组合键可能会或可能不会导致腕管综合症，以及与 Microsoft Word 相匹敌的代码膨胀。如果你习惯使用 Pico 或 Nano 或 Joe 或 Notepad++或 Gedit 或 Kate，或者其他任何东西，你可以在一个月左右的时间内习惯使用 Emacs。真的只是另一个编辑。打哈欠。

Vi 是另一回事。这是一种伪装成编辑器的编辑文本的编程语言。如果你试图像普通的文本编辑器一样使用它，你会吃亏的。如果你处理文本编辑的杂务，比如将代码分解成函数，你就开始理解 Vi 了。

## 模式和运动

正如 Al 所指出的，vi 和 Vim(以下简称 Vim，因为它有一些我非常想念的简洁的附加功能)使用了模态的概念。有一种“插入模式”，你可以在其中输入文本。在普通编辑器中，您总是处于插入模式。在 Vim 中编辑时，大部分时间花在“正常模式”上，在这种模式下，击键就像命令一样，四处移动光标、剪切、粘贴、查找、替换、创建宏、将一个 HTML 标记更改为另一个标记，以及一般的编辑。打字和编辑之间的区别是 Vim 哲学的核心，它们是根本不同的活动。

当你启动 Vim 时，它会告诉你输入`:help`并通过一个教程告诉你如何移动光标。你应该去做那件事——那就是它存在的目的。这不会让你成为大师，但你会学到基础知识。不要让*而不是*到处说你“知道如何使用 Vim”。你只会看起来很傻。你将知道如何移动光标，剪切和粘贴，输入和编辑文本。简而言之，你会像在 Emacs 中的猴子一样编辑。

## 编程文本编辑

Vim 的真正秘密是正常模式用法是一种介于人类语言和编程语言之间的语言。它有动词、形容词和名词(或功能、修饰语和宾语)。你的工作是弄清楚如何用这些大多是单个字符的命令来表达你的文本编辑愿望。

就拿`c`来说吧，这个命令“改变”了一些文本。它本身什么也不做——它需要一个对象。但是如果您输入`caw`(“改变一个单词”)，光标下的单词会被删除，Vim 进入插入模式，等待您输入替换单词，然后按 Escape 键返回正常模式。如果你想改变整个句子，`cas`会删除它，然后你重新输入。想改变圆括号内的一个`C`函数的所有参数？`ci)`“括号内的变化”。(`ca)`删除整个东西，括号和所有。)数字也适合。如果你想改变接下来的五个单词，`c5w`随你便。语法是模块化的和可扩展的。从这个意义上说，很好学。

[![the-shining-3_7-movie-clip-all-work-and-no-play-1980-hd-4lq_mju4qhwmp4-shot0001](img/f7ca6a99e23b9c98811f955da053b151.png)](https://hackaday.com/wp-content/uploads/2016/08/the-shining-3_7-movie-clip-all-work-and-no-play-1980-hd-4lq_mju4qhwmp4-shot0001.jpg) 可爱的小把戏。但是这里有个笑点:`.`。Period 作为一个整体重复最后的编辑操作。因此，如果你只是将一个单词改为“Hackaday”并返回到正常模式，`cawHackaday<Esc>`，并且你将光标放在另一个单词上，输入`.`也会将其转换为“Hackaday”。将移动命令放入混音中，`w`会将光标移动到下一个单词的开头。现在，交替使用`.`和`w`会将文档中的每个单词都变成“Hackaday”。只用了两把钥匙。想想看，如果杰克·尼科尔森拥有维姆和`.`指挥权，他在《闪灵》中表现疯狂的效率会有多高。

这听起来没什么用，但是想想有多少次你通过将所有名为“foo()”的函数改为“getFooInstantanceMethod()”来重构代码。当然，Vim 中有一个“普通的”搜索和替换功能，但是大多数时候你实际上并不需要它。为什么？因为`/foo`搜索“foo”然后`caw`会改变光标下的单词。搜索是一个运动，可以用`;`重复。交替`;`和`.`变得与搜索和替换相同，只有搜索和替换部分是(几乎)任意的编辑动作。你不需要键入“y”和“n”来改变或不改变每一个匹配，你只需点击`;`直到你到达你想要的地方，然后键入`.`。

关于这个话题有太多要说的了，这是 StackOverflow 的*[经典跑题。Vim 的要点是文本编写(在插入模式下)只是输入，编辑器在这方面帮不了你什么。另一方面，文本编辑(在正常模式下)通常由重复的动作组成。Vim 是围绕着将这些操作视为单个单元并使其易于重复和链接在一起而构建的。如果你是一名程序员，这听起来很像我们称之为编程的活动——将一个大任务分解成函数并运行它们。如果你懂编码，你就能学会理解 Vim。](http://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim)*

 *## 视觉和命令模式

事实上，在你掌握 Vim 的道路上，你还想知道更多的模式。视觉模式允许您首先选择文本区域，然后再对其应用命令。它对于一次性的功能很有用，但是视觉模式的选择很难转化为通用的功能，所以我不像以前学习的时候那样经常使用它。然而，有一些有用的插件很好地利用了视觉模式。

命令模式是真正的 Vim 将 geek 赶出去的地方。本质上是 [ed，古行编辑](https://en.wikipedia.org/wiki/Ed_(text_editor))。`:17,25d`删除第 17 行到第 25 行，不移动光标。`:-3t.`复制当前行上方的第三行。`:v/foobar/s/thang/thing/g`将文档中不包含“foobar”的所有行中的“thang”更改为“thing”。这也是你可以使用你储存在灰质中的所有正则表达式的地方。

另一方面，像全局搜索和替换、删除或复制整行这样的简单事情在命令行上也很简单。`%s/one/two/gc`将所有出现的“一”更改为“二”,并确认-您的标准搜索和替换。(`%`指定整个文档。您也可以在这里使用行号范围。)当然还有打开文件进行编辑的`:e`，以及保存当前文件并退出的`:wq`。您不需要了解很多命令行模式的命令，但是有一些非常有用。

## 寄存器和宏

过一会儿，你会想要理解[寄存器](http://vimcasts.org/blog/2013/11/registers-the-good-the-bad-and-the-ugly-parts/)。Vim 将文本(或命令)存储在寄存器中，就像编程语言中的变量一样。您可以在寄存器中剪切和粘贴，前十个寄存器实际上是一个剪切缓冲区。寄存器是一个很好的地方，可以存储您正在剪切的文本，但不确定您是否想要扔掉。`"zdi}`将删除函数括号内的所有代码，但保存在寄存器“z”中。可以随时用`"zp`粘贴回来。想粘贴你五次删除前删除的那个东西吗？键入`:reg`查看所有寄存器及其值。

你也可以像宏一样在寄存器中记录和回放一系列 Vim 命令；毕竟，Vim 命令大多只是字母。`q`开始和结束一个宏记录，因此`qw`会将一个宏记录到寄存器“w”中。你可以稍后用`@w`回放。当然，宏的功能和编写宏的人一样强大。(是的，寄存器加上文本缓冲区就是[图灵完成](https://github.com/divVerent/vi-turing)。不要走极端。)我只用几个宏，但是那些我确实用的，我一直在用。

例如，这里有一个我每天使用一百万次的宏。我在 [Markdown](https://en.wikipedia.org/wiki/Markdown) 写黑客日志，然后编译成 HTML 格式发布。Markdown 中的一个链接是这样的:`[link text]([https://www.example.com](https://www.example.com))`。`S]f]a(<Esc>"+pa)<Esc>`用“[]”对包围当前选定的文本，找到右“]”，添加左括号，离开插入模式，粘贴剪贴板的内容，添加右括号，并返回正常模式。(是的，我花了一段时间才开始工作。)但现在，我在浏览器中复制一个链接，选择文本，在 Vim 中键入`@l`，我就获得了该网站的降价链接。

## 插件

像任何有价值的编辑器一样，Vim 也具有不可思议的可扩展性，如果有任何不能宏执行的特性，人们总是可以为它编写一个插件。在我看来， [Vimscript](http://learnvimscriptthehardway.stevelosh.com/) 甚至比 Lisp 更难写，所以我把扩展编写留给其他人。有人已经为几乎所有你想要的东西编写了一个模块。但是不要一开始就疯狂地使用插件。你已经有了学习 Vim 的工作。

当你不得不安装一堆插件时，我的建议是一次添加一个插件，并使用它，直到你完全理解每个插件。下面是我运行的，按照合理的顺序安装并学习它们: [vim-sensible](https://github.com/tpope/vim-sensible) 、 [vim-airline](https://github.com/vim-airline/vim-airline) 、[vim-disable](https://github.com/tpope/vim-abolish)、 [ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim) 、 [UltiSnips](https://github.com/SirVer/ultisnips) 、 [vim-surround](https://github.com/tpope/vim-surround) 、 [vim-easy-align](https://github.com/junegunn/vim-easy-align) 。

## 最好的 Vim 命令

如果您已经使用了 Vim，但是没有充分使用下面的命令，那么您的生活方式就不正确。

*   `I`和`A`分别在行前或行尾插入和追加文本。
*   `m`和“`设置标记并跳回它们。这对于轻松跳过一个长文档来说是无价的。
*   `g;`回到上次编辑的位置。这就是“在去别的地方之前，从我离开的地方开始”。是金的。但这还不是全部——它会跟踪您的编辑历史，以便您可以返回到五次编辑之前。并且`g,`在编辑历史中向前向后移动。
*   `CTRL-]`跳转到光标下函数定义的位置，`CTRL-t`返回。想深入多深就深入多深——点击`CTRL-t`直到它不再工作，这将让你回到你开始的地方。(你需要一个[标签文件](https://en.wikipedia.org/wiki/Ctags)来完成这项工作。)对我来说，这完全是 Eclipse 这样的 IDE 的一半价值，内置的，屏幕更少混乱。
*   IDE 的另一半是长变量名或函数名的制表符补全。这是在 Vim 中用`CTRL-n`和`CTRL-p`上下滚动可能的列表来完成的。如果您正在使用一个标记文件，或者如果您在 Vim 中打开了带有其他定义的文件，它将为您完成这个名称。
*   `gg=G`跳到文档顶部(`gg`)并自动缩进(`=`)，直到文档结束(`G`)。这使得你所有的左括号和右括号排成一行，并且很容易发现你忘记的那一个。
*   撤消最后一个命令。`CTRL-r`重做。`:earlier 2m`恢复到两分钟前的状态。如果您最终撤销、编辑，然后想要撤销一些以前的更改，您可以。`g+`和`g-`将在撤销树上上下移动。事情变得[复杂](http://vim.wikia.com/wiki/Using_undo_branches)。
*   搜索命令`/`和`f`作为复合命令中的一个动作至关重要。`df,`删除第一个逗号之前的所有内容。`d/foo`允许您删除，直到“foo”上的第一场(交互式)比赛。如果你愿意的话，这可以代替许多其他动作。
*   `:r`读入文件。`:!`在 shell 中运行命令。`:r!`将命令的输出粘贴到你的文档中。`:r!ls whatever*`通常比输入文件名要快。我不打算开始谈论[通过任意的外壳脚本](http://www.softpanorama.org/Editors/Vimorama/vim_running_external_commands.shtml)运行你的文本的能力有多独特。

## Vi 无处不在！

一旦你习惯了 Vim 的移动命令，你就永远被宠坏了。你当然可以使用鼠标，但是当你表现好的时候，你很少会这么做。把手放在琴键上会快很多。几乎每个 Vim 的铁杆用户都会将 Escape 键(返回到正常模式)重新映射到某个方便的地方。我的是原来的大写字母锁，就在我的左手小指下面。(实际上，我使用 [xcape](https://github.com/alols/xcape) 将它与 Control 复用在一起。)是的，这是极端的，但这比人们为了避免从 Emacs 得到腕管而做的事情要好得多，Emacs 是为了在一个实际上已经不存在的键盘上工作而设计的。

如果在 Unix 上使用 Bash shell，`set -o vi`将使 readline [的行为几乎像 vi](http://www.catonmat.net/blog/bash-vi-editing-mode-cheat-sheet/) 一样。你的浏览器可以被虚拟化:火狐的 [Vimperator](http://www.vimperator.org/) 和 [Pentadactyl](http://5digits.org/pentadactyl/) 或者 Chrome 的 [cVim](https://github.com/1995eaton/chromium-vim) 、 [vimium](http://vimium.github.io/) 和 [ViChrome](https://chrome.google.com/webstore/detail/vichrome/gghkfhpblkcmlkmpcpgaajbbiikbhpdi?hl=en) 应该可以做到。如果你想全力以赴， [qutebrowser](https://qutebrowser.org/) 是目前最好的原生 Vim 风格浏览器，而且很快会变得更好。

搜索“vi keybindings ”,你会发现它们在从 Visual Studio 到 Eclipse 到 Emacs 的所有系统中都受到支持。为什么 Emacs [有 Vi 仿真模式](http://www.billharlan.com/pub/emacs/)，而 Vim 没有 Emacs 仿真模式？想一想，你会意识到编辑战已经赢了。

习惯 Vim 需要一段时间。变得真正优秀需要一个程序员的心态和一些积极的实践。从 1994 年到 2011 年，我用 Emacs 写代码、论文、授课费用和学术论文。从 2011 年开始，我用 Vim 写了更多的代码、一本书、电子邮件和我为 Hackaday 写的所有东西。我仍然可以改进，尽管五年来我每天使用它六到八个小时，但我每个月都会增加新的技巧。Vim 很深，就像任何真正值得深入的东西一样，但它是值得的，因为总是有更多的东西。不要相信任何告诉你他们“了解”Vim 的人。`:wq`。

## 资源

关于 Vim 真的有太多要说的了。这里有一些很好的资源:

*   如果你刚刚开始
*   [Vim 常见问题解答](http://vimhelp.appspot.com/vim_faq.txt.html)
*   [Vim 提示 Wiki](http://vim.wikia.com/wiki/Vim_Tips_Wiki)
*   网上许多好的教程之一
*   一些小抄:([一张](http://vimsheet.com/)、[两张](http://vim.rtorr.com/)、[三张](http://vimcheatsheet.com/)、[四张](http://www.angelwatt.com/coding/notes/vim-commands.html))
*   一个[视频](https://www.youtube.com/watch?v=wlR5gYd6um0)把中间的 Vimmers 推到边缘*
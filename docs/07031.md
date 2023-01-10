# 用 ANTLR 进行语言解析

> 原文：<https://hackaday.com/2017/09/07/language-parsing-with-antlr/>

有许多项目需要定制的语言解析器。如果你需要一些标准的东西，你可以从互联网上的某个地方下载代码。如果你需要一些定制的东西，你可以考虑阅读[Federico Tomassetti 的]关于使用 [ANTLR 构建一个完整的基于解析器的系统](https://tomassetti.me/getting-started-with-antlr-building-a-simple-expression-language/)的教程。[Frederico]也为他的书扩展了这些材料，但是仍然有很多可以从八篇博客文章中获得。

他的语言，桑迪，足够复杂，可以作为一个很好的例子，但不是复杂到难以理解。除了帖子，你还可以在 [GitHub](https://github.com/ftomassetti/LangSandbox) 上找到代码。

实现代码是 Java，但是即使你打算使用另一种语言，你仍然可以学到很多东西。这些文章将带您构建一个词法分析器(将文本分解成标记的部分)、解析器、处理语法高亮和自动补全、创建抽象语法树等等。

示例编译器生成 Java 字节码，因此它可以生成可以在 Java 可以运行的任何地方运行的输出。

如果你正在使用 C，你可以考虑查找 lex 和 yacc 或者 flex 和 bison 来得到相似的结果。如果你想解析 C 或 C++，你可能也会对使用 LLVM 作为一种非常特殊的解析器感兴趣。无论哪种方式，定制语言都是推动您的[定制 CPU](https://hackaday.com/2015/07/31/build-your-own-cpu-thats-the-easy-part/) 项目的入场券。
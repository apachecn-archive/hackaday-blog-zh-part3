# 来自 Github 的众包参考设计

> 原文：<https://hackaday.com/2015/11/19/crowdsourcing-reference-designs-from-github/>

大量开源硬件项目正在 Github 上进行，Eagle 是这些设计中最受欢迎的工具之一。【TomKeddie】在深圳黑客营想到了在 Github 中搜索包含特定部分的 Eagle 文件，以及一种刮取有用部分的方法。

危险原型公司的人用这个建立了 Github 硬件搜索工具。只需输入一个零件号，如“ATmega328P”，您将收到一个使用该零件的设计列表。然后，您可以研究该设计，并将其作为您自己项目的参考。您也可以抓取零件的库文件。

当然，这也有一定的局限性。最明显的是缺乏质量控制。不能保证你找到的设计是可行的，甚至是已经建成的。此外，它只适用于 Eagle 6+文件，因为以前的版本不是 XML。你可以在危险原型上阅读更多关于工具[的设计。](http://dangerousprototypes.com/2015/11/12/search-github-projects-by-component-find-design-references/)
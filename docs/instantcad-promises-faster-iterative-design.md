# InstantCAD 承诺更快的迭代设计

> 原文：<https://hackaday.com/2017/08/06/instantcad-promises-faster-iterative-design/>

任何产品的设计过程都必然是一个迭代的过程。通常，原型被建模或建造，并且进行改变以克服问题和改进设计。这可能是一个乏味的过程，这是麻省理工学院的 CSAIL[试图用 instant CAD](http://news.mit.edu/2017/reshaping-computer-aided-design-instantcad-0724)加速的一个过程。

基本思想是将分析工具作为插件集成到现有的 CAD 软件中。可以创建设计，然后对其进行参数化修改，同时在屏幕上以近乎实时的方式更新分析。想象一下，模拟一个扳手，然后拖动滑块来改变长度和宽度，同时实时观察应力集中的变化。该工具似乎主要使用某种有限元分析，尽管该论文也显示了分析流体流动的例子。

该软件令人印象深刻，但也有一些警告。像任何计算机分析一样，必须进行认真的验证工作以确保其有效性。我们怀疑更复杂的几何图形可能会导致不准确的模拟。它不是那种会让生命和肢体处于危险中的工具，但我们可以看到，当你想快速了解某些参数变化会产生什么样的影响时，它在设计基本对象方面有很大的用途。

另一个主要的失望是，虽然这个工具看起来很棒，但它似乎没有以任何形式公开提供。这是因为大学和复杂的知识产权要求，还是因为未来商业化的潜力，谁也说不准。不管怎样，你可以在这里阅读[会议论文](http://people.csail.mit.edu/aschulz/optCAD/a11-schulz.pdf)或者查看下面的视频。或者你也可以阅读一下[有限元分析在 3D 打印机切片器上的应用。](http://hackaday.com/2016/04/07/a-look-into-the-future-of-slicing/)

 [https://www.youtube.com/embed/45YLK7vbL3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/45YLK7vbL3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


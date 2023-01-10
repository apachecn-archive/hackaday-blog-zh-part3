# 使用 Arduino 读取 Amiga 软盘

> 原文：<https://hackaday.com/2017/07/21/read-amiga-floppies-using-an-arduino/>

所以你花了青春在 Amiga 500+前学习你的手艺，但四分之一世纪后，你只剩下一台坏掉的电脑和一堆你不能再读的软盘。该怎么办呢？这就是[Rob Smith]发现自己的处境，由于一些破解 Amiga 软盘的商业解决方案相当昂贵，[他决定尝试制作自己的](http://amiga.robsmithdev.co.uk/)。

当他深入研究他所使用的个人电脑软驱的物理接口，以及控制它的 Arduino 所需要的时间时，他的文章是一篇引人入胜的文章。他在让自己的代码足够快地完成任务时面临一些挑战，并采用了一些优化技术。[他的 Arduino 和 Windows](http://amiga.robsmithdev.co.uk/download) 代码都是开源的，可以从他的 GitHub 库下载。未来的计划包括支持 [FDI](https://en.wikipedia.org/wiki/Amiga_Disk_File#FDI) 光盘格式以及 ADF，并增加写入光盘的能力。

这些年来，我们已经向您展示了许多 Amigas，但在我们的档案中，可能最相关的是这个 [Raspberry Pi 软盘仿真器](http://hackaday.com/2013/11/26/raspberry-pi-emulates-an-amiga-500-floppy-drive/)和这个用于归档光盘收藏的[软盘自动加载器。](http://hackaday.com/2012/03/31/floppy-autoloader-takes-the-pain-out-of-archiving-5000-amiga-disks/)

Via [黑客新闻](https://news.ycombinator.com/item?id=14816927)。
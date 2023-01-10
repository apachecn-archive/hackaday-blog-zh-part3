# IBM 1401 再次运行 FORTRAN II

> 原文：<https://hackaday.com/2018/02/11/ibm-1401-runs-fortran-ii-once-more/>

不可否认，IBM 1401 是一款经典电脑。作为 IBM 最“实惠”的大型机之一，它统治了 20 世纪 60 年代的小型商业计算世界。不幸的是，计算机通常不被视为珍贵的传家宝，只有少数这种机器存活至今。计算机历史博物馆有两台机器。一个来自德国，另一个是 2008 年在康涅狄格州的地下室找到的。[CuriousMarc]和博物馆团队的其他成员一直在努力修复 1401，他们已经达到了一个相当重要的里程碑——他们现在可以编译和运行 FORTRAN II 代码。

让 1401 运行 FORTRAN II 本身就是一项了不起的成就。最困难的部分是处理 729 真空柱磁带驱动器。该团队花了数年时间构建了一个硬件模拟器来代替真正的驱动器。仿真器由运行 windows 的旧 PC 驱动。磁带图像存储为文件，可以像真正的 729 一样加载、倒带和运行。

仿真器很棒，但是[Mark]和他的团队希望它能在真实的硬件上运行。他们首先必须重新创建一个 FORTRAN 编译器磁带。他们在 1401 上运行一个磁带复制器程序，然后在他们的仿真器上加载编译器的映像。计算机忠实地将图像复制到一个真正的磁带驱动器上。

该团队还需要一套穿孔卡片的 FORTRAN 源代码来编译和运行。FORTRAN 手册中的第一个例子是一个[希尔伯特矩阵](https://en.wikipedia.org/wiki/Hilbert_matrix)程序。该小组本来可以用打孔机为程序打孔，但这是一个费力且容易出错的过程。一个错误，他们将不得不重新打一整张卡片——就像使用没有涂改液或改错色带的旧打字机一样。相反，他们将源文件输入电脑，然后将文件转换成磁带图像。一个小程序指示 1401 在卡片上打出源代码。

在关键时刻，首先在视频中显示，1401 从磁带上读取 FORTRAN II，从穿孔卡片上提取源代码，编译，运行，然后在其行式打印机上打印结果。所有的原始硬件就像 1959 年一样一起歌唱。

如果你还没去过[计算机历史博物馆](http://www.computerhistory.org/)，那就去看看吧！它也是[西部](https://hackaday.com/2017/08/10/2017s-vcf-west-is-another-beloved-trip-down-memory-lane/)复古计算节的举办地。

 [https://www.youtube.com/embed/uFQ3sajIdaM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uFQ3sajIdaM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


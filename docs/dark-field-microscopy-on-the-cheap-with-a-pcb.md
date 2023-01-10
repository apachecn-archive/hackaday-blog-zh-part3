# 带 PCB 的廉价暗场显微镜

> 原文：<https://hackaday.com/2018/05/15/dark-field-microscopy-on-the-cheap-with-a-pcb/>

你想用昂贵的显微镜在暗场里看东西，这似乎是一个悖论。正如【IMSAI Guy】[解释的](https://www.youtube.com/watch?v=BPqRMVvQYTU)，暗场显微镜不会让物体变暗。它使主体周围的区域变暗。卖掉昂贵的显微镜后，他发现自己失去了这种能力，所以他决定做一个便宜的。你可以在下面的视频中看到他是如何做到的。

暗场显微镜通过丢弃直接穿过样品或直接从样品反射的光，提供了更好的对比度和分辨率。你看到的唯一的光是散射的光。如果你想象一个普通的显微镜，你可以想象一个光锥从顶部或底部射出。圆锥的尖端撞击样品，然后向外扩散进入另一个光锥。映入你眼帘的——嗯，实际上是目镜——是那个圆锥体发出的所有光线。在暗场仪器中，照明锥是中空的——光只是一个环。这意味着任何没有被样品散射的光都会被物镜上的光阑阻挡。当没有样本时，就没有未被阻挡的光，所以你会看到一个“暗场”

通过样品折射(从下方)或从特征反射(从上方)的光将在穿过物镜的中空区域聚集，您将看到图像。你可能会惊讶地发现，你的办公桌上可能已经有了一块暗场技术。可以在玻璃表面工作的光学计算机鼠标使用了同样的技术。如果你想看一些例子和它如何工作的图表，我们做了一个类似的[低技术模式](https://hackaday.com/2018/05/12/pimp-my-scope/)的帖子。还有[维基百科](https://en.wikipedia.org/wiki/Dark-field_microscopy)。

便宜地做到这一点的秘密是得到一个桶上有点生锈的二手暗场物镜，然后用定制的 PC 板修改它们，以创建一个 LED 环形灯。这不同于通常的照明器，通常的照明器通过遮光板发出光线来阻挡内部光线。在这种情况下，由于 led 的布置，光被制成环形。

对于显微镜的其余部分，一个非常便宜的玩具显微镜给了它的生命，并适合持有修改后的光发生物镜。几个适配器完成了廉价的暗场显微镜。这里没有目镜，但是有一个摄像头将视频传送到你的电脑上。

 [https://www.youtube.com/embed/BPqRMVvQYTU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BPqRMVvQYTU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们感到失望的是，在那个视频中没有显微镜的视频，但是如果你看看下面的视频，你可以看到[作用中的显微镜](https://www.youtube.com/watch?v=R6HF5mqdu-w)。那个展示晶体管拆卸的视频本身就很有趣。还有一段用显微镜拍摄的 [40X 图像](https://www.youtube.com/watch?v=MVntTURSr18)的视频。

 [https://www.youtube.com/embed/R6HF5mqdu-w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R6HF5mqdu-w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们以前见过 [LED 显微镜照明](https://hackaday.com/2018/01/14/not-so-simple-led-upgrade-for-microscope/)。如果你不想在接管上花钱，你可以[用 PVC](https://hackaday.com/2017/02/10/microscope-dslr-mount-using-pvc-heat/) 做一些。
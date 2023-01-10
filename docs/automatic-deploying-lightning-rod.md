# 自动部署避雷针

> 原文：<https://hackaday.com/2017/03/11/automatic-deploying-lightning-rod/>

作为黑客、火腿和建筑商，我们经常遇到来自建筑协会和法规的抵制，这些协会和法规认为什么对我们来说是无害的必需品，但对其他人来说会对他们的视线、财产价值造成风险，或者被视为安全隐患。卑尔根县学院机电一体化研究实验室的一名学生发现了住宅、纪念碑和精美建筑的避雷针也存在同样的问题；尽管避雷针已被证明具有保护作用，但人们不想添加难看的避雷针。她的解决方案？[探测风暴何时来临，并在风暴持续期间自动部署避雷针](http://www.instructables.com/id/Automatic-Lightning-Protection-System/?ALLSTEPS)。

为了探测即将到来的风暴，她正在使用一个 [Adafruit BMP085](https://www.adafruit.com/product/391) 气压、温度和海拔传感器(现已被 [BME280](https://www.adafruit.com/products/2652) 取代)监测不断变化的气压，该传感器连接到一个带有电机护罩的 Arduino。如果气压很低，而且趋势一直在下降，那么她就用从卫星天线中抢救出来的马达转动避雷针。当危险减轻时，她又把钓竿转回来。不可否认，避雷针还没有安装，放电电缆的布置也需要小心，但这只是一个开始。你可以在下面的视频中看到它的运行。

我们以前在 Hackaday 上看到过这个问题。在一个案例中，黑客遇到了性能不佳的 HDTV 天线的问题，他们不得不用难看的铝箔覆盖这些天线，所以[用一个更好看、更有效的 DIY 天线代替了它们](http://hackaday.com/2013/07/16/hdtv-antenna-of-a-different-color/)。你自己的“难看的”天线、卫星天线或其他有争议的部署呢？你有没有想过类似的解决方案？如果是这样，我们想听听他们的情况。

 [https://www.youtube.com/embed/xih00aVa8bw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xih00aVa8bw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


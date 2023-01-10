# 检测运行停止标志的汽车(和松鼠跑过屋顶)

> 原文：<https://hackaday.com/2017/04/12/detect-cars-running-stop-signs-and-squirrels-running-across-the-roof/>

在[德文·加夫尼]的房子外面有一个停车标志，很明显，没有人会停下来。为了避免主干道上的交通堵塞和延误，汽车都走[德文·加夫尼]房子后面的路，但他注意到许多汽车都懒得在停车标志前停下来。他有一个树莓派和一个摄像头，所以他设置它们来检测违规车辆。

他的设置非常标准——树莓派和相机指向外面的十字路口。他正在运行 OpenCV，并使用机器学习来检测汽车，并确定它们是否闯了停车标志。他的网站上有一些漂亮的图表，显示了一周中每一天、每一小时违规行为发生的时间。网站上还有一些链接，你可以用它们来帮助训练系统注意到汽车，看到有停车标志的汽车，判断是否有足够的视频来判断是否有违规行为，以及是否有汽车在十字路口逆行。

这是 Pi 和 OpenCV 的一个有趣的用法；不能保证这将帮助[德文·加夫尼]的邻居，但希望给他们一些弹药(假设他们想做一些关于十字路口的事情)。)这是一个便宜且简单的设置，让社区帮助训练这个系统是很好的。要了解更多 OpenCV，请查看这篇关于[拍摄完美跳投](https://hackaday.com/2013/10/13/perfect-jump-shots-with-opencv-and-processing/#more-104997)的文章，或者这篇试图[量化云朵](https://hackaday.com/2013/02/07/quantifying-cloudiness-with-opencv/)的文章。很酷的东西。

[via [reddit](https://www.reddit.com/r/raspberry_pi/comments/636lc3/using_a_pi_3_to_count_cars_running_a_stop_sign)

 [https://www.youtube.com/embed/jPK0Q58wMNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jPK0Q58wMNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


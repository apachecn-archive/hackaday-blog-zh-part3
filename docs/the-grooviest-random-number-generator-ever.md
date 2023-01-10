# 史上最棒的随机数发生器

> 原文：<https://hackaday.com/2018/01/04/the-grooviest-random-number-generator-ever/>

Cloudflare 是那些你一直在使用，但通常不知道的互联网公司之一。您访问的大型网站使用 Cloudflare 来加强对拒绝服务攻击的防御。该公司需要一些真正的随机数作为其安全解决方案，所以它转向一些时髦的老技术:熔岩灯。在他们的办公室里有一面由 100 盏熔岩灯组成的墙，由摄像头监控着。灯的反应是不可预测的，这使得它们可以产生真正的随机数。Cloudflare 的一名员工[Joshua]在最近的一篇博客文章中谈到了系统的技术细节。

你可能会认为这是一个新的和新奇的想法，但事实证明 [LavaRnd](http://www.lavarnd.org/) (或者可能是[LavaRnd](http://lavarand.org/)——如果你阅读下面的评论，会有一些争议)系统已经存在了一段时间。事实上，[我们早在 2005 年](https://hackaday.com/2005/06/05/lava-lamp-random-number-generator/)就报道过。硅图形在 1996 年申请了该系统的专利。

你可能会认为这些熔岩灯会被锁在某个地堡里。事实证明，只要参观一下 Cloudflare 在旧金山的办公室，你就能看到熔岩灯墙。干扰图像的人是随机不可预测性的来源之一。

该公司并不直接使用灯具中的随机数。[Joshua]解释了在重新启动时，每台生产机器如何抓取一大块随机数，并使用它来播种其通常的随机数生成器。这导致了一个有趣的问题，即确保每个人都是他们所说的人，而不依赖于你试图用随机数编造的非常安全的协议。你可以在博客文章中找到解决这个难题的方法。

你可以在下面看到由[汤姆·斯科特]拍摄的 Cloudflare 熔岩墙视频。如果你不需要随机数发生器，也许你可以使用频谱分析仪。

 [https://www.youtube.com/embed/1cUUfMeOijg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1cUUfMeOijg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Ptkwilliams]的提示。
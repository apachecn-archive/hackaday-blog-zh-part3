# 被字幕黑了

> 原文：<https://hackaday.com/2017/05/25/hacked-by-subtitles/>

CheckPoint 研究人员[在公司博客](http://blog.checkpoint.com/2017/05/23/hacked-in-translation/)中发布了一个关于影响几个视频播放器的漏洞的警告。他们发现 VLC、科迪(XBMC)、爆米花时间和 strem.io 都容易受到恶意字幕文件的攻击。通过精心制作字幕文件，他们声称已经成功地完全控制了任何类型的设备，当他们试图加载视频和相应的字幕时，这些设备使用受影响的播放器。

据研究人员称，情况看起来相当严峻:

> 我们估计，目前大约有 2 亿个视频播放器和流媒体工具运行易受攻击的软件，这是近年来报道的最广泛、最容易访问和零阻力的漏洞之一。(……)迄今为止，每个被发现易受攻击的媒体播放器都有数百万用户，我们认为其他媒体播放器也可能易受类似攻击。

你可能想确保你的软件是最新的，其中一个原因是一些媒体播放器自动从几个共享的在线资源库下载字幕。研究人员证明，攻击者可以操纵网站的排名算法，不仅会诱使更多不知情的用户手动下载他的字幕，还会保证他制作的恶意字幕是媒体播放器自动下载的字幕。

目前还没有透露每个视频播放器如何受到影响的更多细节，尽管研究人员确实将细节分享给了每个软件开发人员，以便他们可以解决这个问题。他们报告说，一些问题已经在当前版本中得到解决，而其他问题仍在调查中。在细节出来之前仔细观察并更新你的系统可能是个好主意。

同时，我们可以看看预告片:

 [https://www.youtube.com/embed/vYT_EGty_6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vYT_EGty_6A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


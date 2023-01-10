# 通过电话和命令行轻松定时录像

> 原文：<https://hackaday.com/2018/01/13/__trashed-4/>

一个好的延时视频可以是有用的视觉文档，由于[Tommy]的手机是他拥有的最好的相机，他创建了两个简单的 shell 脚本来[抓取延时图像并将它们组装成一个视频](http://blog.tommy.sh/posts/making-time-lapse-videos-with-an-iphone-by-command-line)。[汤米]的工作只是其他两件事情之间的粘合剂:一个应用程序，它可以将手机变成一个带有本地网络网络服务器的 IP 摄像头，以及根据需要从服务器上抓取静态图像的能力。

他在 iPhone 上使用的应用程序通常提供视频服务，但有一个未记录的功能，即通过在 URL 的末尾添加“/photo”来下载单帧图像，但获取静态图像的能力是智能手机 IP 相机应用程序的常见功能。因此，他的捕获脚本( [GitHub 库，这里是](https://github.com/rocktronica/timelapse))应该只需要很小的改动，就可以与任何 IP 相机应用程序一起工作。

将手机放在工作区上，用几个 shell 脚本创建一个延时，这是结合简单工具获得更好功能的一个很好的例子。这也是一个让旧智能手机发挥额外功能的好方法。见鬼，即使是老式的哑手机也能派上用场；Shmoocon 2017 为我们带来了关于推出自己的 1G 网络的[细节。](https://hackaday.com/2017/01/16/shmoocon-2017-dig-out-your-old-brick-phone/)
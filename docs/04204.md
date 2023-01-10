# 二维码 IP

> 原文：<https://hackaday.com/2016/11/22/ip-over-qr-codes/>

我们已经看到在一些有趣的媒介上建立的网络，但 QR 码必须是一个新的。[Eric Seifert]决定尝试使用 QR 码建立 IP 连接。他用这些视觉代码在两台装有摄像头的电脑之间建立了双向连接。他是一个坚持不懈的家伙，因为这很有效:在他的一个视频中，他展示了两台设备之间的 SSH 连接。

在此过程中，他面临了许多挑战。虽然有大量的代码来读取二维码，但可以编码和读取的数据是有限的。有一种二进制模式可以配合二维码使用，但是真的效率很低。[Eric]决定改用 base32 编码，将数据作为字母数字文本打包到每一帧中。创建和接收的每个 QR 码图像都有编号，因此系统可以跟踪和请求任何丢失的图像。他在保持编码和解码版本之间的数据一致方面也有一些问题，所以他必须在数据工作之前对其进行一些打包。它使用 [Python-pytun](https://pypi.python.org/pypi/python-pytun/0.2) 创建一个携带数据的 TUN/TAP 设备。

连接速度相当慢:在他的演示视频中，两台计算机为 SSH 连接交换密钥需要一分多钟，而[Eric]测量的连接速度约为每秒 100 位。但是，即使能让这样的东西工作，也是一个重大的成就。他已经在 GitHub 上发布了[他的代码。](https://github.com/seiferteric/qrtun)

我们以前介绍过[Eric]的工作:他用一个 iPod FM 发射器创建了一个数据连接。

 [https://www.youtube.com/embed/N_Qr5AP_2wU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/N_Qr5AP_2wU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 远程无线互联网

> 原文：<https://hackaday.com/2017/06/20/long-range-wireless-internet/>

虽然大多数读到这篇文章的人家里都有宽带，但仍有大片地区很少接入互联网。业余无线电操作员[emmynet]最近发现自己就处于这样的情况，他需要在离家 1 公里以外的地方获得无线连接。WiFi 无法完成这项工作，所以[他转向 433 MHz 的串行链路，而不是](http://emmanuelgranatello.blogspot.it/)。([备用链接](http://emmanuelgranatello.blogspot.it/2017/06/sharing-internet-over-long-range.html))

[emmynet]使用了一种廉价的遥测套件，其工作频率比 WiFi 更容易传输长距离。然而，这里的关键不在于硬件，而在于软件。他走老派路线，使用 SLIP — [串行线路互联网协议](https://en.wikipedia.org/wiki/Serial_Line_Internet_Protocol)实现点对点 TCP/IP 连接。所有设置链接的命令都可以在他的项目页面上找到。使用比遥测套件增益更高的天线，也可以实现 1 公里以上的范围。

[编者按:这是我们在 90 年代早期通过电话线上网的方式。还有，你们这些孩子滚出我的草坪！但是，说真的，SLIP 是你工具箱中的一个好工具，尤其是对于 WiFi 会耗尽电池的低功耗设备。]

虽然它不适合[emmynet]的需求，但它可以通过 WiFi 本身实现[极长距离](http://hackaday.com/2017/04/11/esp32-wifi-hits-10km-with-a-little-help/)。然而，这通常需要具有非常高增益的定向天线，并且可能不如低频连接可靠。另一方面，WiFi 链接(理论上)会获得更大的吞吐量，所以这完全取决于你的需求。此外，请注意，在预期用途之外使用这些频率可能需要业余无线电执照。

 [https://www.youtube.com/embed/rR9ixE3_h0A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rR9ixE3_h0A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


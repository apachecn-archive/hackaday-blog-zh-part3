# 通过无线电信号远程登录大多数智能电视

> 原文：<https://hackaday.com/2017/04/06/remotely-get-root-on-most-smart-tvs-with-radio-signals/>

[Rafael Scheel]一名安全顾问发现，[侵入智能电视](https://www.youtube.com/watch?v=bOJ_8QHX6OA)只需要一个廉价的 DVB-T 发射器，发射器必须在目标电视和一些恶意信号的范围内。黑客的工作原理是利用[混合广播宽带电视](https://en.wikipedia.org/wiki/Hybrid_Broadcast_Broadband_TV)信号和众所周知的智能电视上常见的网络浏览器漏洞，智能电视似乎一直在后台运行。

Scheel 受网络安全公司 [Oneconsult](https://www.oneconsult.com/en/) 的委托，创建了该漏洞，该漏洞一旦部署，就给予攻击者完全的 root 权限，使攻击者能够从世界任何地方设置并 SSH 到电视，完全控制设备。一旦被利用，流氓代码甚至不受设备重启和工厂重置的影响。

> 一旦黑客控制了最终用户的电视，他可以通过各种方式伤害用户，其中包括电视可用于攻击家庭网络中的其他设备，或通过电视的摄像头和麦克风监视用户。拉斐尔·谢尔

智能电视似乎正在遭受物联网安全问题的困扰。把你的电视变成一个全视全听的[监视设备](http://hackaday.com/2013/11/13/ask-hackaday-can-you-hack-an-appliance-into-a-spy-device/)向它的主人汇报直接出自 *1984* 。

下面是一段关于这个漏洞的视频以及所有的细节。

 [https://www.youtube.com/embed/bOJ_8QHX6OA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bOJ_8QHX6OA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


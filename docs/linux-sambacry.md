# linux sambacry

> 原文：<https://hackaday.com/2017/05/25/linux-sambacry/>

好消息，Windows 不是唯一一个通过 SMB 远程执行代码的操作系统。Linux 也有自己七年前的版本。/s

这个 Linux 远程执行漏洞( [CVE-2017-7494](https://www.samba.org/samba/security/CVE-2017-7494.html) )从 3.5.0 版本起(自 2010 年起)影响 SMB 网络协议的 Linux 重新实现 Samba。T2 桑巴克里的绰号几乎是不可避免的。

然而，这个 bug 与 Eternalblue 的工作方式无关，eternal blue 是当前版本的 [WannaCry](http://hackaday.com/2017/05/12/massive-cyber-attack-cripples-multiple-uk-hospitals/) 勒索软件打包的漏洞之一。尽管 Eternalblue 本质上是一种缓冲区溢出利用，但 CVE-2017-7494 利用了任意共享库负载。要利用它，恶意客户端需要能够将共享库文件上传到可写共享，然后攻击者就有可能让服务器加载并执行它。Metasploit 漏洞利用模块已经公开，能够针对 Linux ARM、X86 和 X86_64 架构。

解决该缺陷的补丁已经发布到[官方网站](http://www.samba.org/samba/security/)上，Samba 4.6.4、4.5.10 和 4.4.14 已经作为安全版本发布以纠正该缺陷。针对旧版本 Samba 的补丁也是可用的。如果您目前无法应用补丁，解决方法是在您的`smb.conf`的[global]部分添加参数“nt pipe support = no ”,然后重启`smbd`。请注意，这可能会禁用 Windows 客户端的某些预期功能。

与此同时，NAS 供应商开始意识到他们有工作要做。使用 Samba 进行文件共享的不同品牌和型号(很多，如果不是全部，都提供这种功能)如果想要修补这个缺陷，就必须发布固件更新。如果这些设备的固件更新花费的时间和平时一样多，那么这个问题将会持续很长时间。
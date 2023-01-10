# 树莓派，给我寄封信

> 原文：<https://hackaday.com/2016/10/04/raspberry-pi-send-me-a-letter/>

大量运行 Linux 的小型网络板——如 Raspberry Pi——对开发人员来说是个福音。把一台小型廉价计算机放到网络上是很容易的。Linux 拥有大量软件的事实是一把双刃剑。一方面，很有可能你想做的事情都已经做了。另一方面，有些解决方案对于小型嵌入式系统来说有点大。

以电子邮件为例。历史上，Linux 主机充当邮件传输代理，可以为所有用户发送和接收邮件，甚至可能将邮件转发给其他用户。在今天的世界里，这通常是多余的，但是这种能力是存在的。在 Raspberry Pi 中安装大型邮件传输代理是可能的。问题是:你应该吗？

## 你想要什么?

答案当然取决于你想做什么。如果你有一个使用外部邮件服务器(比如 Gmail)发送文本甚至文件的专用板，那么答案是否定的。你不需要一个软件来监听传入的连接，对多个用户进行排序，等等。

幸运的是，如果你知道如何设置和配置，有一些简单的解决方案。关键是要避免那些做所有你不需要的事情的大邮件程序。

## 邮件前端

让我们先解决发送邮件的问题。如果你试图抓取 mailutils 包，你会看到它拖着很多东西，包括 mysql。请记住，这些都不会真正发送邮件。它只是给你一些工具，让邮件准备发送。

幸运的是，bsd-mailx 包的开销要小得多，可以完成这项工作。查看手册页,了解 mailx 有哪些选项；您可以附加文件、设置主题和指定地址。

不过，由于谷歌的安全性，设置 Gmail 有点困难。您将需要 libns3-tools 包中的 certutil 工具。您需要创建一个证书库，导入 Google 的证书，然后为 mailx 设置许多选项。我不建议这样做。不过，如果你坚持的话，你可以在网上找到方向。

## SSMTP

默认情况下，像 mailx 和其他 Linux 邮件命令这样的程序依赖于后端(通常是 sendmail)。这不仅增加了太多的开销，也是一个完整的邮件系统，发送、接收和转发——对我们的小 Pi 计算机来说是多余的。

幸运的是，SSMTP 是可用的，它只发送邮件，是相对轻量级的。您需要一个配置文件来将它指向您的邮件服务器。对于 Gmail，它看起来像这样:

```
#
# Config file for sSMTP sendmail
#
# The person who gets all mail for userids < 1000
# Make this empty to disable rewriting.
root=postmaster

# The place where the mail goes. The actual machine name is required no 
# MX records are consulted. Commonly mailhosts are named mail.domain.com
mailhub=smtp.gmail.com:587

# Where will the mail seem to come from?
rewriteDomain=yourdomain.com

# The full hostname
hostname=yourhostname
AuthUser=YourGmailUserID
AuthPass=YourGmailPassword
UseTLS=Yes
UseSTARTTLS=YES
# Are users allowed to set their own From: address?
# YES - Allow the user to specify their own From: address
# NO - Use the system generated From: address
FromLineOverride=YES
```

您可以使用 mailx 之类的邮件代理，也可以直接使用 ssmtp:

```
ssmtp someone@somewhere.com
```

在标准输入上输入一条消息，并以 Control+D 结束(Linux 的标准文件结尾)。

## 谷歌认证器

只有一个条件。如果你正在使用 Gmail，你会发现谷歌希望你使用更强的认证。如果你使用双因素(即谷歌认证)，这是行不通的。你需要生成一个[应用密码](https://support.google.com/mail/answer/185833)。即使你不是，你也可能需要放松谷歌对你账户上垃圾邮件制造者的[恐惧。你需要打开“访问不太安全的应用程序”设置。如果您不想在您的主要电子邮件帐户上这样做，请考虑创建一个仅用于从 Pi 发送数据的帐户。](https://support.google.com/accounts/answer/6010255)

## 发送文件

根据您使用的邮件软件，有几种方法可以附加文件。然而，mpack 程序使它变得非常简单:

```
mpack -a -s 'Data File' datafile.csv me@hackaday.com
```

上述命令将 datafile.csv 作为附件发送，主题为“数据文件”很简单。

## 接收邮件

如果您想颠倒这个过程，在 Pi 上接收邮件，该怎么办呢？有一个叫 fetchmail 的程序可以从 IMAP 或 POP3 服务器上抓取电子邮件。可以让它只阅读第一封未读邮件，然后发送给你选择的脚本或程序。

您必须构建一个配置文件(或者使用 fetchmailconf 程序来构建它)。例如，这里有一个简单的。fetchmailrc 文件:

```
poll imap.gmail.com
protocol IMAP
user "user@gmail.com" with password "yourpassword" mda "/home/pi/mailscript.sh"
folder 'INBOX'
fetchlimit 1
keep
ssl
```

如果你不介意 fetchmail 在处理后删除邮件，你可以不写“keep”行。该文件应该在您的主目录中(除非您用-f 选项指定),并且它不能被其他用户读写(例如 chmod 600。fetchmailrc)。根据 fetchmail [FAQ](http://www.fetchmail.info/fetchmail-FAQ.html#I9) 的说法，Gmail 存在一些问题，所以你可能需要考虑一些提供的建议。然而，对于像这样简单的任务，你应该能够全部解决。

特别是，mailscript.sh 文件是您可以处理电子邮件的地方。例如，您可能会查找某些关键字命令并采取一些措施(可能使用 ssmtp 进行回复)。

## 特快专递

你可能不会想到树莓派是一个电子邮件机器。然而，事实上它是一个非常普通的 Linux 系统，这意味着你可以使用各种为大型计算机设计的有趣工具。你只需要知道它们的存在。
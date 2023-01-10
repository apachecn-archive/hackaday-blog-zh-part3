# 用谷歌认证器锁定你的树莓皮

> 原文：<https://hackaday.com/2016/09/30/lock-up-your-raspberry-pi-with-help-from-google/>

Raspberry Pi 板(或许多类似的板中的任何一种)可以方便地放在奇怪的地方，与网络对话，收集数据，控制事物，或做任何其他需要微型无风扇计算机完成的任务。当然，任何时候你有一台电脑在网络上，你都在邀请黑客(不是我们这种黑客)闯入。

我们最近看到了[如何通过 Pagekite](http://hackaday.com/2016/09/21/how-to-run-a-pagekite-server-to-expose-your-raspberry-pi/) 使用反向代理建立 ssh 隧道，这样您甚至可以通过防火墙和动态 IP 地址连接到 Pi。你如何阻止一个坏人反复尝试登录，直到他们有访问权限？这可以在任何 Linux 机器上工作，但是对于本教程，我将使用 Raspberry Pi 作为示例设备。在所有情况下，知道如何设置足够的 ssh 安全性对于您接入网络的任何东西都是至关重要的。

## 比密码安全更好

专家告诉你使用好的密码。但是，对于 ssh，最好的方法是完全禁止密码。要做到这一点，您需要在您想要用来连接的机器上创建一个私有和公共证书。然后将公钥复制到树莓 Pi 中。一旦设置完成，您的 ssh 客户机将自动向服务器进行认证。如果你总是使用同一个机器登录，并且你从来没有丢失过你的钥匙，那就太好了。

如果您还没有创建个人密钥对，那么您需要创建一个。您可以在 Linux 上使用 ssh-keygen 命令来做到这一点。您可以要求输入密码来解锁密钥，或者，如果您确定只有您可以访问您的计算机，您可以将其留空。

一旦有了密钥，就可以很容易地用 ssh-copy-id 命令将公钥发送到服务器。例如:

```
ssh-copy-id me@ssh.hackaday.com
```

您使用您的密码最后一次登录，该命令将您的公钥复制到服务器。从那时起，当您在该主机上使用 ssh 时，您将被自动认证。非常方便。

一旦设置了密钥，就可以通过编辑/etc/ssh/sshd_config 来禁止使用常规密码。您需要以下设置:

```
ChallengeResponseAuthentication no
PasswordAuthentication no
UsePAM no
```

这可以防止任何人通过暴力猜测密码来闯入。这也使得设置新用户或从新电脑登录变得更加困难。

## 保存密码；使用两种类型

出于这些原因，关闭密码并不总是一个好主意。更好的想法是使用双因素身份验证。这需要您输入密码和“一次性”验证码。你从哪里得到的代码？

有几个选项，但我将使用来自 Google Authenticator 应用程序的选项。你可以在苹果设备、黑莓手机，当然还有安卓设备上下载这个应用。您可以按照通常的方式为您的设备安装它。诀窍是如何让 Pi 上的 ssh 服务器使用它。

幸运的是，Raspian repos 有一个名为 libpam-google-authenticator 的包可以完成这个任务。不过，用 apt-get 安装它只是技巧的一部分。你需要两样东西。首先，你需要设置你的账户。

### 设置一个谷歌认证账号

要设置您的帐户，您需要登录到您的 Pi 并发出命令 google-authenticator。该程序会问你几个问题，然后生成一个网址，向你展示一个二维码。它还会为您提供一个数字代码。您可以使用其中任何一个来设置您的手机。该命令还将为您提供一些一次性的临时代码，您需要保存这些代码，以防丢失验证器设备。对于任何可以通过 ssh 登录的用户 ID，您都需要这样做(即使是那些通常使用证书的用户)。

### 告诉您的 Pi 要求双因素登录

谜题的另一部分要求您对/etc/pam.d/sshd 和/etc/ssh/sshd_config 进行更改。/etc/pam.d/sshd 的第一行应该是:

```
auth required pam_google_authenticator.so
```

在/etc/ssh/sshd_config 中，您需要确保密码处于打开状态:

```
ChallengeResponseAuthentication yes
PasswordAuthentication yes
UsePAM yes
```

只要确保你不会搞砸任何事情。失去 ssh 服务器可能会阻止您访问机器。我还没有搞砸过，但是我听到的建议是在重启 ssh 服务器(/etc/init.d/sshd restart)时保持 ssh 会话打开，这样如果出现问题，您仍然可以打开 shell 提示符。您也可以考虑运行:

```
/usr/sbin/sshd -t
```

这将在您扣动扳机之前验证您的配置。

顺便说一下，如果您已经使用证书登录，这不会为您带来任何变化。证书验证优先于密码。这确实让测试你的设置变得棘手。您可以强制 ssh 不要像这样使用您的证书:

```
ssh -o PreferredAuthentications=password -o PubkeyAuthentication=no me@ssh.hackaday.com
```

即使对于使用证书的帐户，添加双因素登录将防止对您的密码的暴力攻击，因此请确保为您可以通过 ssh 使用的所有帐户设置。

## 其他保护

您还可以做其他一些事情来帮助保护您的 ssh 连接:

*   禁止 root 登录(编辑/etc/ssh/sshd_config 中的 PermitRootLogin 行；如果你想成为超级用户，你可以用普通帐号使用 sudo)
*   使用非标准的 ssh 端口(在 sshd_config 中编辑端口)
*   考虑安装 fail2ban，它将阻止表现出可疑行为的 IP 地址
*   禁止任何不需要 ssh 访问的用户(在 sshd_config 文件中使用 AllowUsers 或 DenyUsers)
*   将 sshd_config 中的 PermitEmptyPasswords 设置为“否”

不是每个人都同意禁止 root 登录。然而，根据经验，许多攻击者会尝试以 root 用户身份登录，因为几乎每个 Linux 系统都有这个帐户。随机攻击者很难知道我的用户 ID 是 WetSnoopy。

还有许多其他技术，从端口敲门到将用户锁定到他们的主目录。您可以对 ssh 端口上的连接尝试进行速率限制。只有你能决定多少安全是足够的。毕竟，锁好你的钱箱比锁好你的储藏室要好。然而，方便和免费的双因素身份验证可以为您的 Raspberry Pi 或其他基于 Linux 的项目增加高级别的安全性。如果你真的担心，顺便说一句，你也可以强制访问 sudo 的双因素。
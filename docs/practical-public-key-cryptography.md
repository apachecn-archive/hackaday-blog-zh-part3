# 实用公钥密码学

> 原文：<https://hackaday.com/2017/10/18/practical-public-key-cryptography/>

加密是现代通信的支柱之一。您的设备一直在使用加密技术，即使您没有意识到这一点。有如此多的应用程序和系统使用它，很难开始列举它们。从卫星电视到手机，从智能电表到汽车钥匙，从无线路由器到浏览器，从签证到比特币，不胜枚举。

加密史上最大的突破之一是 70 年代公钥密码学或非对称密码学的发明。几个世纪以来，人们一直使用传统的加密方法，加密消息的发送方和接收方必须同意并共享某些密钥或方案。

不对称加密改变了这一点。今天，你可以向任何人发送加密信息。这是通过使用一对密钥来实现的:一个*公钥*和一个*私钥*。密钥属性是这样的，当用公钥加密某个东西时，只有私钥可以解密它，反之亦然。在实践中，这通常是基于数学问题来实现的，这些数学问题不允许像某些整数因式分解、离散对数和椭圆曲线关系这样的有效解决方案。

但是改变游戏规则的是公钥不必保密。这使得加密技术可以用于身份验证——证明某人是谁——以及加密，而不需要您事先交换秘密。在这篇文章中，我将详细介绍如何设置自己，以便世界上的任何人都可以向您发送只有您可以阅读的电子邮件。

## 简而言之，公钥加密

但首先，它在理论上是如何工作的？假设爱丽丝想和鲍勃说话。(没错，又是爱丽丝和鲍勃。)Alice 和 Bob 生成他们各自的密钥对。他们告诉全世界他们的公钥，包括彼此。Alice 现在可以使用 Bob 的公钥来加密只有 Bob 可以读取的消息，只有 Bob 的私钥可以解密该消息，顾名思义，它应该是私有的，只有 Bob 知道。

想象一下，爱丽丝想向世界(或鲍勃)发送一条重要的信息，并证明这条信息来自她？在我们生活的时代，我们如何确定爱丽丝声称发送的信息不是假的？嗯，爱丽丝用她自己的私人钥匙来加密她重要的信息。世界只需要使用 Alice 公钥来解密该消息，因为这是解密它的唯一方法，并且只有拥有 Alice 私钥的人才能加密它，因此证明是 Alice 写了该消息。

## 让我们让爱丽丝开始吧

因此，假设爱丽丝已经安装了 GPG，她将从创建自己的公钥/私钥对开始:

```

alice@wonderland ~ $ gpg --gen-key
gpg (GnuPG) 1.4.20; Copyright (C) 2015 Free Software Foundation, Inc.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
(1) RSA and RSA (default)
(2) DSA and Elgamal
(3) DSA (sign only)
(4) RSA (sign only)
Your selection? 1

RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (2048)

Requested keysize is 2048 bits
Please specify how long the key should be valid.
0 = key does not expire
&lt;n&gt; = key expires in n days
&lt;n&gt;w = key expires in n weeks
&lt;n&gt;m = key expires in n months
&lt;n&gt;y = key expires in n years
Key is valid for? (0)
Key does not expire at all
Is this correct? (y/N) Y

You need a user ID to identify your key; the software constructs the user ID
from the Real Name, Comment and Email Address in this form:
&quot;Heinrich Heine (Der Dichter) &lt;heinrichh@duesseldorf.de&gt;&quot;

Real name: Alice
Email address: alice@wonderland.xyz
Comment: Mushroom
You selected this USER-ID:
&quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot;

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O
You need a Passphrase to protect your secret key.
...
public and secret key created and signed.

pub 2048R/96FE8CE5 2017-10-13
Key fingerprint = B5FF 1BE3 4502 F425 A444 D6EC FBEC 78AE 96FE 8CE5
uid Alice (Mushroom) &lt;alice@wonderland.xyz&gt;
sub 2048R/76E5C437 2017-10-13

```

根据 Alice 的需要，设置密钥过期可能是个好主意。在这个命令之后，最好将密钥的副本导出并存储在安全的地方，最好有冗余。例如，她可以在 USB 驱动器中存储一份拷贝，打印一份硬拷贝并放在保险箱中。

```

alice@wonderland ~ $ gpg --export-secret-key alice@wonderland.xyz &gt; ./alice-gpg-backup.gpg

alice@wonderland ~ $ gpg --export-secret-key -a alice@wonderland.xyz
-----BEGIN PGP PRIVATE KEY BLOCK-----
Version: GnuPG v1

lQPGBFngvxUBCADNVg9j2iNv3FuzscUOe9oZqP0xCk8p9s+ApIDTqD6vZFkXLpYs...
-----END PGP PRIVATE KEY BLOCK-----

```

上述命令执行备份并输出适合打印的 ASCII 版本的私钥。OpenPGP 的私钥实现实际上包含了公钥的完整副本，所以这个备份文件足以恢复密钥对。恢复备份是通过`--import`标志完成的。

## 告诉世界你是谁

现在爱丽丝有了她的钥匙，是时候告诉全世界了。有几种方法可以做这件事。在命令行上:

```

alice@wonderland ~ $ gpg --list-public-keys
/home/alice/.gnupg/pubring.gpg
------------------------------
pub 2048R/96FE8CE5 2017-10-13
uid Alice (Mushroom) &lt;alice@wonderland.xyz&gt;
sub 2048R/76E5C437 2017-10-13

alice@wonderland ~ $ gpg --send-keys 96FE8CE5
gpg: sending key 96FE8CE5 to hkp server keys.gnupg.net

alice@wonderland ~ $ gpg --search-keys 96FE8CE5
gpg: searching for &quot;0x96FE8CE5&quot; from hkp server keys.gnupg.net
(1) Alice (Mushroom) &lt;alice@wonderland.xyz&gt;
2048 bit RSA key 96FE8CE5, created: 2017-10-13
Keys 1-1 of 1 for &quot;0x96FE8CE5&quot;. Enter number(s), N)ext, or Q)uit &gt; q

```

这样，Alice 就在一个已知的 OpenPGP 密钥服务器上发布了她的密钥，任何人都可以访问。(`keys.gnupg.net`是我的发行版的默认设置。)有几个密钥服务器可用于发布公钥，其中一些是同步的。我喜欢用`pgp.mit.edu`。另一种选择是导出带有`--export`标志的公钥，并通过电子邮件发送和/或在几个服务器上手动发布——越多越好。现在，爱丽丝可以对她的信息进行数字签名，并接收发送给她的加密信息。让我们看一个例子:

```

alice@wonderland ~ $ echo &quot;This is a test file&quot; &gt; file.txt
alice@wonderland ~ $ gpg --detach-sign file.txt

You need a passphrase to unlock the secret key for
user: &quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot;
2048-bit RSA key, ID 96FE8CE5, created 2017-10-13

alice@wonderland ~ $ ls -l file*
-rw-rw-r-- 1 alice alice 37 Out 13 15:56 file.txt
-rw-rw-r-- 1 alice alice 287 Out 13 15:56 file.txt.sig

alice@wonderland ~ $ gpg --verify file.txt.sig
gpg: assuming signed data in `file.txt'
gpg: Signature made Sex 13 Out 2017 15:56:23 WEST using RSA key ID 96FE8CE5
gpg: Good signature from &quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot;

alice@wonderland ~ $ echo &quot;The file contents have been tampered&quot; &gt; file.txt

alice@wonderland ~ $ gpg --verify file.txt.sig

gpg: assuming signed data in `file.txt'
gpg: Signature made 13 Out 2017 15:56:23 WEST using RSA key ID 96FE8CE5
gpg: BAD signature from &quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot;

```

当 Alice 希望共享`file.txt`时，她也会共享`file.txt.sig`，这样任何人都可以验证她的签名。所以 Alice 可以签名，但是在她可以给 Bob 发送消息之前，Bob 也必须有一个密钥对，并且在某个地方发布他的公钥或者将它发送给 Alice。让我们假设 Bob 已经这样做了，Alice 将 Bob 的公钥导入到 GPG，要么用`--import`标志，要么从服务器导入`--recv-keys`。如果 Alice 想给 Bob 发送消息，她会发出以下命令:

```

alice@wonderland ~ $ gpg --import bob.asc
gpg: key 81DBD5F6: public key &quot;Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;&quot; imported
gpg: Total number processed: 1
gpg: imported: 1 (RSA: 1)

alice@wonderland ~ $ gpg --list-public-keys
/home/alice/.gnupg/pubring.gpg
------------------------------
pub 2048R/96FE8CE5 2017-10-13
uid Alice (Mushroom) &lt;alice@wonderland.xyz&gt;
sub 2048R/76E5C437 2017-10-13

pub 2048R/81DBD5F6 2017-10-13
uid Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;
sub 2048R/21B662BE 2017-10-13

alice@wonderland ~ $ echo &quot;This is a secret message to Bob&quot; &gt; message.txt
alice@wonderland ~ $ ls -l message*
-rw-rw-r-- 1 alice alice 32 Out 13 16:25 message.txt
alice@wonderland ~ $ gpg -r bob@whatdoesthebobsay.xyz --sign --encrypt message.txt

You need a passphrase to unlock the secret key for
user: &quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot;
2048-bit RSA key, ID 96FE8CE5, created 2017-10-13

gpg: gpg-agent is not available in this session
gpg: 21B662BE: There is no assurance this key belongs to the named user

pub 2048R/21B662BE 2017-10-13 Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;
Primary key fingerprint: 1558 11B0 C87D 0E02 1C8B 304F 4982 D1D3 81DB D5F6
Subkey fingerprint: 6CC7 BC9C D69E 9465 78E4 53E3 A931 7A64 21B6 62BE

It is NOT certain that the key belongs to the person named
in the user ID. If you *really* know what you are doing,
you may answer the next question with yes.

Use this key anyway? (y/N) y
alice@wonderland ~ $ ls -l message*
-rw-rw-r-- 1 alice alice 32 Out 13 16:25 message.txt
-rw-rw-r-- 1 alice alice 678 Out 13 16:25 message.txt.gpg

```

这将使用 Bob 的公钥加密`message.txt`,并使用 Alice 的私钥对文件进行签名。现在，Alice 可以将文件`message.txt.gpg`发送给 Bob，Bob 不仅是唯一能够解密该文件的人，只要他有 Alice 的公钥，他还可以验证该文件是否来自 Alice。让我们看看鲍勃会怎么做:

```

bob@whatdoesthebobsay ~ $ gpg --import alice-public-key.asc
gpg: key 96FE8CE5: public key &quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot; imported
gpg: Total number processed: 1
gpg: imported: 1 (RSA: 1)

bob@whatdoesthebobsay ~ $ gpg --decrypt message.txt.gpg

You need a passphrase to unlock the secret key for
user: &quot;Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;&quot;
2048-bit RSA key, ID 21B662BE, created 2017-10-13 (main key ID 81DBD5F6)

gpg: encrypted with 2048-bit RSA key, ID 21B662BE, created 2017-10-13
&quot;Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;&quot;

This is a secret message to Bob

gpg: Signature made Sex 13 Out 2017 16:19:51 WEST using RSA key ID 96FE8CE5
gpg: Good signature from &quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot;
gpg: WARNING: This key is not certified with a trusted signature!
gpg: There is no indication that the signature belongs to the owner.
Primary key fingerprint: B5FF 1BE3 4502 F425 A444 D6EC FBEC 78AE 96FE 8CE5

```

## 你能信任谁？

您可能已经注意到一条警告消息，指出 Alice key 没有经过可信签名的认证，并且没有迹象表明该签名属于她。如果鲍勃确实知道爱丽丝的密钥来自爱丽丝，他可以签名，GPG 会认为它是可信的。

```

bob@whatdoesthebobsay ~ $ gpg --edit-key alice@wonderland.xyz sign

pub 2048R/96FE8CE5 created: 2017-10-13 expires: never usage: SC
trust: undefined validity: unknown
sub 2048R/76E5C437 created: 2017-10-13 expires: never usage: E
[ unknown] (1). Alice (Mushroom) &lt;alice@wonderland.xyz&gt;

pub 2048R/96FE8CE5 created: 2017-10-13 expires: never usage: SC
trust: undefined validity: unknown
Primary key fingerprint: B5FF 1BE3 4502 F425 A444 D6EC FBEC 78AE 96FE 8CE5

Alice (Mushroom) &lt;alice@wonderland.xyz&gt;

Are you sure that you want to sign this key with your
key &quot;Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;&quot; (81DBD5F6)

Really sign? (y/N) y

You need a passphrase to unlock the secret key for
user: &quot;Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;&quot;
2048-bit RSA key, ID 81DBD5F6, created 2017-10-13

gpg&gt; save
bob@whatdoesthebobsay ~ $ gpg --decrypt message.txt.gpg

You need a passphrase to unlock the secret key for
user: &quot;Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;&quot;
2048-bit RSA key, ID 21B662BE, created 2017-10-13 (main key ID 81DBD5F6)

gpg: encrypted with 2048-bit RSA key, ID 21B662BE, created 2017-10-13
&quot;Robert (Nope) &lt;bob@whatdoesthebobsay.xyz&gt;&quot;
This is a secret message to Bob
gpg: Signature made Sex 13 Out 2017 16:19:51 WEST using RSA key ID 96FE8CE5
gpg: checking the trustdb
gpg: 3 marginal(s) needed, 1 complete(s) needed, PGP trust model
gpg: depth: 0 valid: 8 signed: 2 trust: 0-, 0q, 0n, 0m, 0f, 8u
gpg: depth: 1 valid: 2 signed: 0 trust: 1-, 1q, 0n, 0m, 0f, 0u
gpg: next trustdb check due at 2019-03-19
gpg: Good signature from &quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot;

```

警告将会消失。但是为什么会有警告呢？到目前为止，有人发了一封邮件声称有爱丽丝的公钥，但是鲍勃怎么知道是他认识的那个爱丽丝呢？或者初始公钥交换没有被截获？尽管公钥加密消除了分发秘密密钥的需要，但公钥必须分发给他们想要与之通信的其他人，并且如果加密也用于认证，则公钥的出处很重要。

那么鲍勃有什么选择呢？Bob 可以与 Alice 面对面，在那里 Alice 向他保证她的密钥(或她的密钥指纹)是正确的，Bob 可以通过如上例中的签名将其标记为可信。有时面对面是不可能的，或者你正在和一个你并不真正认识的人交谈。Bob 也可以选择信任特定的密钥服务器，这通常是非常安全的。如果 Bob 不想选择信任任何密钥服务器，还有另一种方法。

### 信任之网

GnuPG 通过一种被称为[信任网](https://en.wikipedia.org/wiki/Web_of_trust)的机制来解决这个问题。在信任网络模型中，验证公钥的责任委托给了您信任的人。这不同于普通的公钥基础设施(PKI)方法，因为 PKI 允许每个证书仅由一方签名:认证机构(CA)。相比之下，OpenPGP 身份证书(包括公钥和所有者信息)可以由其他用户进行数字签名，这些用户通过签名确认该公钥与证书中所列人员的关联。

甚至还有被称为[密钥签名聚会、](https://en.wikipedia.org/wiki/Key_signing_party)的活动，在这些活动中，用户带着他们的密钥和身份文档聚集在一起，并相互签署密钥。基本上，随着越来越多的人签署一个密钥，你就越能确定这个密钥来自它所声称的那个人。

## 我收回所有的话

最后，Alice 创建一个撤销证书可能是个好主意。如果 Alice 丢失了她的密钥或者她认为密钥被泄露，则可以使用撤销证书。发布它是为了通知其他人不应再使用该公钥。被撤销的公钥仍然可以用于验证 Alice 过去所做的签名，但是它不能用于加密将来发送给 Alice 的消息。这也不影响对过去发送给 Alice 的消息进行解密的能力，如果她仍然拥有密钥的话。

```

alice@wonderland ~ $ gpg -a --gen-revoke alice@wonderland.xyz

sec 2048R/96FE8CE5 2017-10-13 Alice (Mushroom) &lt;alice@wonderland.xyz&gt;

Create a revocation certificate for this key? (y/N) y
Please select the reason for the revocation:
0 = No reason specified
1 = Key has been compromised
2 = Key is superseded
3 = Key is no longer used
Q = Cancel
(Probably you want to select 1 here)
Your decision? 0
Enter an optional description; end it with an empty line:
&gt; revoke!
&gt;
Reason for revocation: No reason specified
revoke!
Is this okay? (y/N) y

You need a passphrase to unlock the secret key for
user: &quot;Alice (Mushroom) &lt;alice@wonderland.xyz&gt;&quot;
2048-bit RSA key, ID 96FE8CE5, created 2017-10-13

Revocation certificate created.

Please move it to a medium which you can hide away; if Mallory gets
access to this certificate he can use it to make your key unusable.
As with the private key, it is smart to print this certificate and store it away, just in case
your media become unreadable. But have some caution: the print system of
your machine might store the data and make it available to others!

-----BEGIN PGP PUBLIC KEY BLOCK-----
Version: GnuPG v1
Comment: A revocation certificate should follow

iQEmBCABAgAQBQJZ5N6XCR0AcmV2b2tlIQAKCRD77Hiulv6M5XnuB/41jjJCVx/S
...
-----END PGP PUBLIC KEY BLOCK-----

```

上面的代码演示了如何生成一个撤销证书。

## “这太混乱了！”

我明白了。我知道。用户不想通过命令行加密东西，担心证书和信任模型。乍一看，这似乎有点令人不知所措，但幸运的是，最终用户可以使用易于使用的软件解决方案来解决您的基本公钥加密需求。这是一个很长的列表，我很确定我们的读者根据你的互联网使用和操作系统有很多建议。让我们听听他们的评论吧！

例如，要保护电子邮件，有几种选择。如果使用雷鸟，可以安装 Enigmail。它应该可以在 Linux、Windows、Mac 和 SunOS/Solaris 上运行。Outlook 用户，找 gpg4o 或者 gpg4win。苹果邮件有 GPGTools。Android 有 K9 和 R2Mail2，iOS 有 iPGMail。如果你不使用特定的电子邮件客户端，而是使用网络邮件，你没有被遗漏，你可以尝试 Mailvelope。Mailvelope 是 Chrome 和 Firefox 的扩展，它实现了 OpenPGP，可以在常规的网络邮件客户端上工作。

关于邮件加密，你可以看到有很多选择。可能有一个 OpenPGP 实现可供您选择的电子邮件客户端使用，这是一个为您已经习惯的软件选择解决方案的问题，并从那里开始。所以如果你还没有使用加密，你现在的借口是什么？

去创造你的密钥对，与世界分享！现在就做吧，在下一次密码学革命[量子计算](https://hackaday.com/2015/09/29/quantum-computing-kills-encryption/)之前，把它全部杀死。
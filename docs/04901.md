# 使用 SSH 授予任何人对您的电脑的临时权限

> 原文：<https://hackaday.com/2017/02/05/grant-anyone-temporary-permissions-to-your-computer-with-ssh/>

对于 Linux 用户来说，这是一个超级可爱的技巧。如果你玩过宋承宪，你就会知道这是自面包片以来最神奇的东西。为了挖隧道进去，挖隧道出来，甚至只是为了安全地打开一个壳，这是蜜蜂的膝盖。如果你在多台电脑上工作，你了解`ssh-copy-id`吗？在偶然发现获胜者之前，我们已经使用 SSH*年*。

无论如何，[费利佩·拉夫拉蒂]的[ssh-allow-friend](https://github.com/felipe-lavratti/ssh-allow-friend)脚本本身很简单，但它增加的功能很容易值得入场费。它所做的只是查找你朋友的公钥(目前只从 GitHub)并将它临时添加到你的`[authorized_keys](http://man.he.net/man5/authorized_keys)`文件中。当您按 ctrl-C 退出脚本时，它会删除这些键。只要您的朋友拥有与公钥相对应的私钥，他或她就可以作为您的用户帐户登录。

这里真的没有什么是你不能用手做的。该脚本只是自动创建和删除公钥，并使用 GitHub 作为您朋友身份的仲裁者。如果你确实知道他们的 GitHub 用户名*，并且他们已经将他们的公钥附加到账户上，这是一个非常精简和简单的过程。(我们自己尝试了一下，结果发现我们没有将一个公共 SSH 密钥与我们的帐户关联起来。)也就是说，它可以扩展到任何提供公钥的可信位置。*

 *在我们发霉的档案中寻找一篇关于 SSH 技巧和诀窍的文章，我们找不到。这可能吗，评论者们？这是我们必须解决的问题，所以[把你最喜欢的 SSH 魔术](http://hackaday.com/submit-a-tip/)发给我们。与此同时，我们会通过翻出[Al Williams]对 MOSH(一个移动 SSH 客户端)的精彩[评论来满足你对更多 Hackaday 的渴望。](http://hackaday.com/2016/11/01/ssh-enters-the-mosh-pit/)*
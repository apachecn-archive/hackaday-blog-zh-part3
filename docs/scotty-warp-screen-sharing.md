# 斯科特曲速屏幕共享。

> 原文：<https://hackaday.com/2017/06/10/scotty-warp-screen-sharing/>

在协同工作时，能够看到某人的屏幕是很方便的。对于 GUI，有很多选项。有几种方法可以共享终端屏幕(如 screen、tmux 和 tmate)。现在有一个新的基于 Go 语言的终端共享程序，由开发者 spolu 开发，名为 [Warp](https://github.com/spolu/warp) 。

与其他一些解决方案不同，Warp 很简单，只专注于共享一个 shell 会话，并且不需要 ssh 或中央服务器(某种程度上)。尽管没有使用 ssh，但是机器之间的连接是安全的。但是，如果您真的担心安全性，请注意，任何人只需连接会话名称(未公布)即可。可能应该很难猜测。

另一方面，在默认情况下，人们只能查看您的屏幕会话，因此至少攻击者不能只是开始输入恶意命令。但是，您可以授权某人取得控制权，但在这种情况下，您会想要非常确定您知道您允许谁使用您的电脑。

Go 将在 Raspberry Pi 上运行，因此在那里安装应该很容易。你至少需要 1.7 版本的 Go。您还应该设置 GOROOT 和 GOPATH 环境变量。您可能还想将 GOPATH 添加到系统路径中，以便更容易运行 warp(和其他 Go 可执行文件)。

虽然自述文件说没有中央服务器，但看起来它确实使用 warp.link 服务器来管理连接请求。我们不是 Go 专家，但我们假设对代码的检查会看到 warp.link 服务器解析名称并移交连接。但是，如果你真的有安全意识，你应该确保。

如果不介意 ssh 的话，随时可以用 tmux 的[这个分叉。也可以直接用 tmux](https://tmate.io/) [或者 screen](https://www.howtoforge.com/sharing-terminal-sessions-with-tmux-and-screen) (见下面视频)。这些方法都不会像 [Mosh](https://hackaday.com/2016/11/01/ssh-enters-the-mosh-pit/) 那样健壮，但是那是一个不同的用例。或者如果你敢的话，你可以把你电脑的钥匙给别人。

 [https://www.youtube.com/embed/norO25P7xHg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/norO25P7xHg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 从世界任何地方控制 Alexa Echo

> 原文：<https://hackaday.com/2017/03/09/control-alexa-echo-from-anywhere-in-the-world/>

如果你不在你的 Alexa Echo、Dot 或 Tap 设备的听力范围内，并且需要从世界任何地方命令它，你最有可能使用方便的移动应用程序或网络界面来控制它。出于某种奇怪的原因，如果你宁愿在世界任何地方使用语音命令，你仍然可以使用 Alexa Listens 或 Reverb 等应用程序来完成。我们会是第一个指出这些并说“这不是黑客”的人。但是[pat dhens]的方法是无可指责的！他发布了如何在世界任何地方遥控 Alexa Echo 的细节。黑客的简短版本——他正在使用一个树莓 Pi，上面附有一个扬声器，可以通过文本到语音转换程序命令他的 Alexa Tap。

长的版本也很短。用户使用 VPN，如 [OpenVPN](https://openvpn.net/) ，登录到 Alexa 设备所在的家庭网络。然后，使用 VNC 连接到 Raspberry Pi 来访问它的外壳。最后，用户发出一个文本命令，它被树莓 Pi 上的“[节](http://www.cstr.ed.ac.uk/projects/festival/)”程序转换成语音。输出通过 Raspberry Pi 的 3.5 毫米音频输出插孔连接到外部扬声器。这就是全部了。您刚刚从世界各地向您的 Alexa 发出了语音命令。

我们猜测，这可能会保护你的声带免受过度叫喊的伤害。他甚至制作了一个短片来证明这是有效的。现在它只需要一个麦克风来听 Alexa，将语音转换为文本，然后将它传输回世界各地的你，以完成循环。

我们不确定，但他认为这次入侵会让他统治世界。祝你好运。

 [https://www.youtube.com/embed/8bq7VdBPM8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8bq7VdBPM8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


# 用 Python 为你的机器人创建一个不和谐的网络钩子

> 原文：<https://hackaday.com/2018/02/15/creating-a-discord-webhook-in-python/>

Discord 是一个类似 IRC 的聊天平台，所有年轻酷孩子都在上面闲逛。 [Discord](https://discordapp.com/) 最初是作为在线游戏中的一种交流方式，现在已经发展到几乎任何可以想象的话题都有服务器的地步。这种惊人增长的原因之一是创建和调节自己的 Discord 服务器是多么容易:只需在网站或移动应用程序中点击“+”图标，就可以了。

作为一个长期使用 IRC 的人，我最初对不和谐并不感兴趣。它看起来像是我们已经用了几十年的同类产品，但是有着公认的光滑的用户界面。在使用了几个月后，我加入了从游戏到火箭科学的服务器，我不能说我对 Discord 的最初印象是不准确的:它绝对只是一个现代的 IRC。但是我也意识到我可以接受。

但这不是一个不和谐的评论或邀请加入我为我的战场排设置的服务器。在本文中，我们将看看创建一个简单的“机器人”是多么容易，您可以将它插入到一个不和谐的服务器中，并使用它做有用的工作。由于任何人都可以免费创建一个持久的 Discord 服务器，因此通过简单地向服务器发送消息，这是一个用于物联网监控和日志记录的有趣平台。

## 实际例子

[![](img/a8e6b9232ea8d04cc6bddc08417d09d4.png)](https://hackaday.com/wp-content/uploads/2018/02/discordbot_feat.png)

Weather bot posting to my Discord channel

我不想在你如何在你的项目中使用不和谐的细节上陷得太深，我把它留给读者去想象。但是举个例子，假设你想创建一个气象监测站，每小时向你的 Discord 服务器发布一次当前温度和天空图片。

我们还假设温度检测在后台进行，并作为变量`CURRENT_TEMP`供我们的代码使用，图像`"latest_img.jpg"`也在当前目录中自动弹出，我们的 Python 脚本可以在该目录中找到它。

## 设置 Discord 服务器

如前所述，建立一个 Discord 服务器非常容易。你真正要做的就是给这个东西起个名字，然后点击“创建”。顺便说一句，你应该通过 Discord web 界面在你的计算机上设置服务器，因为下面提到的所有选项目前在移动应用程序中都不可用。

一旦你创建了它，你就需要进入 webhooks 的服务器设置。在这里，您将创建 webhook 条目，并获得脚本将消息发送到服务器所需的身份验证令牌。

每个 webhook 都需要有自己的名字，你可以给它们单独的图标来美化一下。该配置还会询问您希望 webhook 访问哪个通道，如果您计划将大量数据转储到服务器中，这可以让您很好地细分。

webhook 配置的最后一部分是最重要的，因为它为您提供了 webhook 将使用的 URL。URL 包含身份验证令牌和 ID:

`discordapp.com/api/webhooks/***WEBHOOK_ID***/***WEBHOOK_TOKEN***`

## 软件环境

如前所述，我将用 Python 来做这件事，因为这也是现在酷孩子正在做的事情。你能想到的几乎任何语言都有 Discord 库，所以如果你想在你选择的语言中做一些类似的事情，这应该不是问题，服务器端的设置看起来还是一样的。

所需的两个库是曾经流行的[请求](http://docs.python-requests.org/en/master/)，它将为我们处理 HTTP 方面的事情，以及 [discord.py](https://github.com/Rapptz/discord.py) ，它是 Python 最流行的 Discord API 包装器。请注意，我们需要使用 discord.py 的开发版本来实现这一点，因为稳定版本目前不支持 webhook。

## 代码

使用这些库向 Discord 服务器发送消息实际上非常简单，基本实现只需要几行代码:

```

#!/usr/bin/env python3
import requests
import discord
from discord import Webhook, RequestsWebhookAdapter, File

# Create webhook
webhook = Webhook.partial(WEBHOOK_ID, WEBHOOK_TOKEN,\
 adapter=RequestsWebhookAdapter())

# Send temperature as text
webhook.send(&quot;Current Temp: &quot; + CURRENT_TEMP)

# Upload image to server
webhook.send(file=discord.File(&quot;latest_img.jpg&quot;))

```

这就是全部了。执行这段代码应该会从之前创建的 webhook bot 向 Discord 服务器发送一条消息。

## 最后的想法

[![](img/ad4b0868681cd687ef20ddf268986b34.png)](https://hackaday.com/wp-content/uploads/2018/02/discordbot_battlespy1.png)

Automatically generated stats posted to Discord

Discord 拥有适用于所有主流移动和桌面操作系统的原生应用程序，以及一个非常精致的网络界面，你可以在任何一台装有现代网络浏览器的电脑上使用它，而无需安装任何东西。这种普遍性和易用性使它成为一个有趣的平台，不仅仅是聊天游戏。使用 Discord 进行远程监控和日志记录意味着您和您希望邀请的任何人都可以获得关于您想要的任何内容的即时通知和更新。

就我个人而言，我正在使用一个类似的设置，通过几个 Python 脚本和一个在 Pi Zero 上运行的 cron 作业，将我的战场排自动生成的统计数据直接发布到我们每周五早上的 Discord 聊天中。但唯一真正的限制是你的想象力。
# 带 NodeMCU 的简单以太坊自动售货机

> 原文：<https://hackaday.com/2018/05/10/simple-ethereum-vending-machines-with-nodemcu/>

最近，我们介绍了如何使用 Etherscan API 通过 NodeMCU 从以太坊区块链查询数据(钱包余额)。在存储和内存是个问题的嵌入式系统中，这是一种非常有用的从区块链中检索信息的方法。

尽管它有一些限制。最值得注意的是，它以一定的时间间隔轮询 API，以检索信息是否已经更改。我希望能够比这更有效地接收数据，并且足够快地让简单的自动售货机成为可能。虽然我们以前看过基于比特币的红牛自动售货机的[视频，但它们需要 NFC 卡才能使用。](http://www.youtube.com/watch?v=-YuE2g09Q4w)

如果我们能够足够快速可靠地接收有关以太坊交易的信息，我们就可以建造一个类似的自动售货机，而不需要 NFC 卡作为中介。只需通过一些方法发送到一个地址，并收到货物！

事实证明，我们可以通过 NodeMCU 使用 [WebSocket](http://nodemcu.readthedocs.io/en/master/en/modules/websocket/) 做到这一点。与 HTTP 一样，WebSocket 是一种使用 TCP 连接(通常通过端口 80)的通信协议，但它允许全双工通信。换句话说，您可以建立到服务器的连接，并且无需轮询服务器就可以发送/接收消息。

[和前面的例子](http://hackaday.com/2018/05/02/using-blockchain-explorer-apis-on-nodemcu/)一样，我们将使用一个运行 Lua 的 NodeMCU。您可能希望参考它来获得关于屏幕的编译选项和信息，这在本例中是相同的。与前一篇文章不同，你不需要来自 [Etherscan](http://etherscan.io/) 的 API 密匙来使用这个服务(至少现在还不需要)。像往常一样，我们将从连接 WiFi 开始:

```

wifi.setmode(wifi.STATION)
wifi.setphymode(wifi.PHYMODE_B)
station_cfg={}
station_cfg.ssid=&quot;Your SSID&quot;
station_cfg.pwd=&quot;Your Password&quot;
station_cfg.save=true
wifi.sta.config(station_cfg)

```

用 WebSockets 连接到服务器很容易，但是由于我们不使用 HTTP，我们必须删除`https://`并用`ws://`替换它。(注意:不是`wss://`，因为我们还没有启用加密。)

ws:connect(' ws://socket . ethers can . io/ws handler ')

接下来，我们需要报告连接何时建立，作为运行附加代码的触发器。如果连接建立失败，它将返回一个错误代码。以合理的方式处理这些错误代码是一个很好的特性，但是我们将在后面处理:

```

ws:on(&quot;connection&quot;, function(ws)
    print('got ws connection')
    end)

```

现在，我们需要扩展上面的内容来订阅一个 Eth 地址，并添加一些新的代码来在事务发生时做一些事情。请注意，API 要求您在连接后 60 秒内订阅一个地址。它还声明您必须每 20 秒向服务器发送一次 ping 事件来保持连接，因此我们需要为此设置一个循环计时器。

如果您使用的是 ESPlorer，您可以通过输入`=ws:send('{"event": "ping"}')`并按 send 来手动发送 ping 请求。这是测试连接状态的有用方法。

我使用的地址似乎有频繁的交易，所以测试是合理的。请注意，坐着等待一个事务发生来测试代码会造成一个缓慢的开发周期，所以这里需要一些耐心。

```

ws = websocket.createClient()
ws:on(&quot;connection&quot;, function(ws)
    print('got ws connection')
    ws:send('{&quot;event&quot;: &quot;txlist&quot;, &quot;address&quot;: &quot;0x2a65aca4d5fc5b5c859090a6c34d164135398226&quot;}')
    end)

ws:on(&quot;receive&quot;, function(_, msg, opcode)
    print('got message:', msg, opcode)
    end)

```

您应该会看到如下所示的内容。第一条消息是简单的连接确认，第二条消息确认您对某个地址的订阅，第三条消息是交易发生时您收到的消息。您可以通过一台连接的设备订阅多达 30 个地址！注意，数据都是 JSON 格式的，这是我们稍后要利用的。

```

got message: {&quot;event&quot;:&quot;welcome&quot;} 1
got message: {&quot;event&quot;:&quot;subscribe-txlist&quot;, &quot;status&quot;:&quot;1&quot;, &quot;message&quot;:&quot;OK, 0x2a65aca4d5fc5b5c859090a6c34d164135398226&quot;} 1
got message: {&quot;event&quot;:&quot;txlist&quot;,&quot;address&quot;:&quot;0x2a65aca4d5fc5b5c859090a6c34d164135398226&quot;,&quot;result&quot;:[{&quot;blockNumber&quot;:&quot;5532531&quot;,&quot;timeStamp&quot;:&quot;1525098009&quot;,&quot;hash&quot;:&quot;0xe5ec497cb5b38811e8bf5db67a056a2bdd4aa9b68df5c8e8225cb300cbcfa413&quot;,&quot;nonce&quot;:&quot;3363391&quot;,&quot;blockHash&quot;:&quot;0xf446f77d92ed29c221e8451b8048113969ed305a7dd49177e10b422e8e2c4bda&quot;,&quot;transactionIndex&quot;:&quot;172&quot;,&quot;from&quot;:&quot;0x2a65aca4d5fc5b5c859090a6c34d164135398226&quot;,&quot;to&quot;:&quot;0xec5fdfba35c01c6ad7a00085e70e8f30cd121597&quot;,&quot;value&quot;:&quot;24418350000000000&quot;,&quot;gas&quot;:&quot;50000&quot;,&quot;gasPrice&quot;:&quot;4000000000&quot;,&quot;input&quot;:&quot;0x&quot;,&quot;contractAddress&quot;:&quot;&quot;,&quot;cumulativeGasUsed&quot;:&quot;7896403&quot;,&quot;gasUsed&quot;:&quot;21000&quot;,&quot;confirmations&quot;:&quot;1&quot;}]} 1

```

这是一堆乱七八糟的事务数据，不幸的是，感兴趣的数据在“结果”字段中——这是嵌套的 JSON。[在上一篇文章](http://hackaday.com/2018/05/02/using-blockchain-explorer-apis-on-nodemcu/)中，我们使用优秀的`sjson`模块将简单的 JSON 转换成 Lua 表。在验证消息类型是一个事务(`txlist`)之后，我们将做同样的事情。

```

ws:on(&quot;receive&quot;, function(_, msg, opcode)
    print('got message:', msg, opcode)
    ok, ethdata = pcall(sjson.decode, msg)
    if ok then
        msgtype = (ethdata[&quot;event&quot;])
        if msgtype == &quot;txlist&quot; then
...

```

NodeMCU 文档特别指出嵌套的 JSON 会导致内存不足的错误。出于这个原因，我们在解码 JSON 消息时使用`pcall`(受保护的调用)来包含任何这样的错误。接下来，我们提取嵌套在“结果”字段中的“值”字段的内容:

```

if msgtype == &quot;txlist&quot; then
    wei = ethdata.result[1].value
    print (wei)
    eth = wei/1000000000000000000
    print (eth)
    end

```

我花了几个小时才弄明白如何处理嵌套表，但最终它实际上非常干净和简单——我只是在犯傻。现在，我们需要添加一个基本条款来处理 websocket 关闭时的错误:

```

ws:on(&quot;close&quot;, function(_, status)
    print('connection closed', status)
    print('Reconnecting...')
    ws = nil -- required to Lua gc the websocket client
    tmr.alarm(0,4000,tmr.ALARM_SINGLE,transact) -- This reconnects after 4 seconds
end)

```

最后，我们将代码封装在几个函数中——首先，一个函数建立连接，订阅正确的地址，并在有事务时发出通知。接下来，我们需要一个来显示转移的 Eth 的数量。最后，我们需要一个每 20 秒或更短时间调用一次的“ping”功能来保持连接。总的来说，这比预期的更加健壮，并且还没有遇到错误。点击这里查看[的完整代码清单](https://ghostbin.com/paste/bkeg7)。请注意，我还在上面添加了一点代码来与 128×32 的有机发光二极管屏幕接口，[与我们之前使用的](http://hackaday.com/2018/05/02/using-blockchain-explorer-apis-on-nodemcu/)相同。

既然有效，那就考虑 im/实际应用吧。这是一个实时显示以太坊交易的好方法，比如说，如果你做直播，接受 Eth 捐赠，并希望它们触发一些奇特的东西。或者，你可以做一个有点不安全的自动售货机。显然，建立并运行一个安全的 WebSocket 是下一步要做的事情。

你也可以设置一个定时器，定时器的长度取决于接收到的以太网的数量。如果有人付费，这将允许像公共广告这样的事情暂时消失。(请不要这样！)也许一个会议室出租，用这种方式控制电源？Hackerspace 会员付费？一辆电动自行车用电收费？

在任何情况下，在我的国家使用加密货币作为支付形式都是不合法的，所以我现在还不能实现上面的任何例子。如果你有更好的应用，请在评论中分享！
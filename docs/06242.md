# Espressif ESP8266 上的实用物联网加密技术

> 原文：<https://hackaday.com/2017/06/20/practical-iot-cryptography-on-the-espressif-esp8266/>

Espressif ESP8266 芯片组使三美元的“物联网”开发板成为经济现实。根据流行的自动固件构建网站 nodeMCU-builds ，在过去的 60 天里，该平台有 13，341 个定制固件版本。其中，只有 19%支持 SSL，10%包含加密模块。

我们经常批评物联网领域缺乏安全性，并经常报道 T2 僵尸网络和 T4 其他攻击，但是我们会按照我们要求的标准来管理我们的项目吗？我们会止步于发现问题，还是成为解决方案的一部分？

本文将重点关注使用运行 NodeMCU 固件的流行的 ESP8266 芯片将 AES 加密和散列授权函数应用于 MQTT 协议。我们的目的不是提供一个复制/粘贴的万灵药，而是一步一步地经历这个过程，在这个过程中识别挑战和解决方案。其结果是一个端到端加密和认证的系统，防止沿途窃听和有效数据的欺骗，而不依赖于 SSL。

我们知道也有更强大的平台可以轻松支持 SSL(例如，Raspberry Pi、Orange Pi、FriendlyARM)，但让我们从我们大多数人身边最便宜的硬件和适合我们许多项目的协议开始。如果需要，您可以在 AVR 上实现 AES。

## 理论

MQTT 是运行在 TCP/IP 之上的轻量级消息协议，经常用于物联网项目。客户端设备订阅或发布主题(例如传感器/温度/厨房)，这些消息由 MQTT 代理转发。更多关于 MQTT 的信息可以在他们的网页或[我们自己的入门系列](http://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)中找到[。](http://mqtt.org/)

除了用户名/密码认证之外，MQTT 协议没有任何内置的安全特性，因此通常使用 SSL 通过网络进行加密和认证。然而，SSL 对 ESP8266 的要求可能相当高，启用时，留给应用程序的内存会少得多。作为一种轻量级的替代方案，您可以只加密正在发送的数据负载，并使用会话 ID 和散列函数进行身份验证。

一种简单的方法是使用 Lua 和 NodeMCU [加密模块](http://nodemcu.readthedocs.io/en/master/en/modules/crypto/)，它支持 [CBC 模式](https://en.wikipedia.org/w/index.php?title=Block_cipher_mode_of_operation&section=6#Cipher_Block_Chaining_.28CBC.29)下的 AES 算法以及 HMAC 哈希函数。正确使用 AES 加密需要三样东西来生成密文:消息、密钥和初始化向量(IV)。消息和键是简单的概念，但是初始化向量值得讨论。

当您使用静态密钥对 AES 中的消息进行编码时，它将始终产生相同的输出。例如，用密钥“1234567890ABCDEF”加密的消息“usernamepassword”可能会产生类似“E40D86C04D723AFF”的结果。如果您使用相同的密钥和消息再次运行加密，您将得到相同的结果。这使您面临几种常见类型的攻击，尤其是模式分析和重放攻击。

在模式分析攻击中，您使用给定数据将总是产生相同密文的知识来猜测不同消息的目的或内容，而实际上不知道密钥。例如，如果消息“E40D86C04D723AFF”在所有其他通信之前发送，人们可能会很快猜到这是一次登录。简而言之，如果登录系统过于简单，发送该数据包(重放攻击)可能足以将您标识为授权用户，混乱随之而来。

IVs 使得模式分析更加困难。IV 是与密钥一起发送的一段数据，它修改了最终的密文结果。顾名思义，它在数据进入之前初始化加密算法的状态。发送的每条消息都需要不同的 IV，以便重复的数据加密成不同的密文，一些密码(如 AES-CBC)要求它是不可预测的——实现这一点的实际方法是每次都将其随机化。IVs 不一定要保密，但通常会以某种方式混淆它们。

虽然这可以防止模式分析，但对重放攻击没有帮助。例如，重新传输一组给定的加密数据仍然会复制结果。为了防止这种情况，我们需要验证发送者的身份。我们将为每条消息使用一个公共的、伪随机生成的会话 ID。这个会话 ID 可以由接收设备通过发送到 MQTT 主题来生成。

在一些常见的用例中，防止这些类型的攻击非常重要。互联网控制的炉子是存在的，且撇开可疑的效用不谈，[如果它们不使用不安全的命令就好了](http://hackaday.com/2017/04/20/half-baked-iot-stove-could-be-used-as-a-remote-controlled-arson-device/)。其次，如果我从一百个传感器记录数据，我不希望任何人用垃圾填充我的数据库。

## 实用加密

在 NodeMCU 上实现上述内容需要一些努力。除了您的应用程序所需的任何其他模块之外，您将需要[已编译的](http://nodemcu-build.com/)固件来包含“加密”模块。不需要 SSL 支持。

首先，让我们假设您连接到一个 MQTT 代理，如下所示。您可以将它作为一个独立于加密的函数来实现，以保持整洁。客户端订阅一个`sessionID`通道，该通道发布适当长的伪随机会话 id。你可以加密它们，但这不是必要的。

```

m = mqtt.Client(&quot;clientid&quot;, 120)

m:connect(&quot;myserver.com&quot;, 1883, 0,
function(client)
print(&quot;connected&quot;)
client:subscribe(&quot;mytopic/sessionID&quot;, 0,
function(client) print(&quot;subscribe success&quot;) end
)
end,
function(client, reason)
print(&quot;failed reason: &quot; .. reason)
end
)

m:on(&quot;message&quot;, function(client, topic, sessionID) end)

```

接下来，节点 ID 是帮助识别数据源的一种便捷方式。你可以使用任何你想要的字符串: `nodeid = node.chipid()`。

然后，我们设置一个静态初始化向量和一个密钥。这仅用于混淆与每条消息一起发送的随机化初始化向量，不用于任何数据。我们还为数据选择了一个单独的键。这些密钥是 16 位十六进制的，用你的替换就行了。

最后，我们需要一个哈希函数的密码，我们稍后会用到。长度合理的字符串就可以了。

```

staticiv = &quot;abcdef2345678901&quot;
ivkey = &quot;2345678901abcdef&quot;
datakey = &quot;0123456789abcdef&quot;
passphrase = &quot;mypassphrase&quot;

```

我们还假设你有一些数据来源。对于本例，它将是从 ADC 读取的值。 `data = adc.read(0)`

现在，我们生成一个伪随机初始化向量。一个 16 位的十六进制数对于伪随机数函数来说太大了，所以我们把它分成两半(16^8 减 1)并连接起来。

```

half1 = node.random(4294967295)
half2 = node.random(4294967295)
I = string.format(&quot;%8x&quot;, half1)
V = string.format(&quot;%8x&quot;, half2)
iv = I .. V

```

我们现在可以运行实际的加密了。在这里，我们加密当前的初始化向量、节点 ID 和一条传感器数据。

```

encrypted_iv = crypto.encrypt(&quot;AES-CBC&quot;, ivkey, iv, staticiv)
encrypted_nodeid = crypto.encrypt(&quot;AES-CBC&quot;, datakey, nodeid,iv)
encrypted_data = crypto.encrypt(&quot;AES-CBC&quot;, datakey, data,iv)

```

现在我们应用散列函数进行认证。首先，我们将`nodeid`、`iv`、`data`和会话 ID 组合成一条消息，然后使用我们之前定义的密码计算 HMAC·SHA1 散列。我们将它转换成十六进制，使它对于任何调试都更易于阅读。

```

fullmessage = nodeid .. iv .. data .. sessionID
hmac = crypto.toHex(crypto.hmac(&quot;sha1&quot;, fullmessage, passphrase))

```

既然加密和身份验证检查都已就绪，我们可以将所有这些信息放在某个结构中并发送出去。这里，为了方便起见，我们将使用逗号分隔的值:

```

payload = table.concat({encrypted_iv, eid, data1, hmac}, &quot;,&quot;)
m:publish(&quot;yourMQTTtopic&quot;, payload, 2, 1, function(client) p = &quot;Sent&quot; print(p) end)

```

当我们在实际的 NodeMCU 上运行上面的代码时，我们会得到类似这样的输出:

```
1d54dd1af0f75a91a00d4dcd8f4ad28d,
d1a0b14d187c5adfc948dfd77c2b2ee5,
564633a4a053153bcbd6ed25370346d5,
c66697df7e7d467112757c841bfb6bce051d6289

```

总之，加密程序如下所示(为了清楚起见，MQTT 部分被排除在外):

```

nodeid = node.chipid()
staticiv = &quot;abcdef2345678901&quot;
ivkey = &quot;2345678901abcdef&quot;
datakey = &quot;0123456789abcdef&quot;
passphrase = &quot;mypassphrase&quot;

data = adc.read(0)
half1 = node.random(4294967295)
half2 = node.random(4294967295)
I = string.format(&quot;%8x&quot;, half1)
V = string.format(&quot;%8x&quot;, half2)
iv = I .. V

encrypted_iv = crypto.encrypt(&quot;AES-CBC&quot;, ivkey, iv, staticiv)
encrypted_nodeid = crypto.encrypt(&quot;AES-CBC&quot;, datakey, nodeid,iv)
encrypted_data = crypto.encrypt(&quot;AES-CBC&quot;, datakey, data,iv)
fullmessage = nodeid .. iv .. data .. sessionID
hmac = crypto.toHex(crypto.hmac(&quot;sha1&quot;,fullmessage,passphrase))
payload = table.concat({encrypted_iv, encrypted_nodeid, encrypted_data, hmac}, &quot;,&quot;)

```

## [通信]解密

现在，您的 MQTT 代理不知道也不关心数据是否加密，它只是传递数据。因此，订阅该主题的其他 MQTT 客户机需要知道如何解密数据。在 NodeMCU 上，这相当容易。只需 [通过逗号](http://lua-users.org/wiki/SplitJoin) 将接收到的数据拆分成字符串，并做如下操作。请注意，此端将生成会话 ID，因此已经知道它。

```

staticiv = &quot;abcdef2345678901&quot;
ivkey = &quot;2345678901abcdef&quot;
datakey = &quot;0123456789abcdef&quot;
passphrase = &quot;mypassphrase&quot;

iv = crypto.decrypt(&quot;AES-CBC&quot;, ivkey, encrypted_iv, staticiv)
nodeid = crypto.decrypt(&quot;AES-CBC&quot;, datakey, encrypted_nodeid,iv)
data = crypto.decrypt(&quot;AES-CBC&quot;,datakey, encrypted_data,iv)
fullmessage = nodeid .. iv .. data .. sessionID
hmac = crypto.toHex(crypto.hmac(&quot;sha1&quot;,fullmessage,passphrase))

```

然后比较收到的和计算的 HMAC，不管结果如何，通过生成一个新的会话 ID 来使该会话 ID 无效。

## 同样，在 Python 中

作为一个小小的变化，考虑一下我们将如何在 Python 中处理解密，如果我们在同一个虚拟机上有一个 MQTT 客户机，作为分析数据或将其存储在数据库中的代理。让我们假设您已经收到了作为字符串“有效载荷”的数据，来自于类似优秀的用于 Python 的 Paho MQTT 客户端的东西。

在这种情况下，在传输之前，在 NodeMCU 上对加密数据进行十六进制编码是很方便的。因此，在 NodeMCU 上，我们将所有加密数据转换为十六进制，例如: `encrypted_iv = crypto.toHex(crypto.encrypt("AES-CBC", ivkey, iv, staticiv))`

发布一个随机化的 sessionID 不会在下面讨论，但是使用 os.urandom()和 [Paho MQTT 客户端](http://pypi.python.org/pypi/paho-mqtt/1.1)是很容易的。解密的处理方式如下:

```

from Crypto.Cipher import AES
import binascii
from Crypto.Hash import SHA, HMAC

# define all keys
ivkey = '2345678901abcdef'
datakey = '0123456789abcdef'
staticiv = 'abcdef2345678901'
passphrase = 'mypassphrase'

# Convert the received string to a list
data = payload.split(&quot;,&quot;)

# extract list items
encrypted_iv = binascii.unhexlify(data[0])
encrypted_nodeid = binascii.unhexlify(data[1])
encrypted_data = binascii.unhexlify(data[2])
received_hash = binascii.unhexlify(data[3])

# decrypt the initialization vector
iv_decryption_suite = AES.new(ivkey,AES.MODE_CBC, staticiv)
iv = iv_decryption_suite.decrypt(encrypted_iv)

# decrypt the data using the initialization vector
id_decryption_suite = AES.new(datakey,AES.MODE_CBC, iv)
nodeid = id_decryption_suite.decrypt(encrypted_nodeid)
data_decryption_suite = AES.new(datakey,AES.MODE_CBC, iv)
sensordata = data_decryption_suite.decrypt(encrypted_data)

# compute hash function to compare to received_hash
fullmessage = s.join([nodeid,iv,sensordata,sessionID])
hmac = HMAC.new(passphrase,fullmessage,SHA)
computed_hash = hmac.hexdigest()

# see docs.python.org/2/library/hmac.html for how to compare hashes securely

```

## 结束，开始

现在，我们有了一个通过 MQTT 服务器向另一个 ESP8266 客户机或运行 Python 的更大系统发送加密的、经过身份验证的消息的系统。如果您自己实现了这一点，仍然有一些重要的细节需要处理。这些密钥都存储在 ESP8266s 的闪存中，因此您需要控制对这些设备的访问，以防止逆向工程。密钥也存储在接收数据的计算机的代码中，这里运行 Python。此外，您可能希望每个客户端都有不同的密钥和密码。这是大量需要安全保存的秘密资料，并可能在必要时进行更新。解决密钥分发问题留给有兴趣的读者做练习。

最后，写一篇涉及密码学的文章最可怕的事情之一就是*在互联网上出错的可能性*。这是一个相当直接的应用测试和真实的 AES-CBC 模式与 HMAC，所以它应该是非常坚实的。尽管如此，如果你在上面发现任何有趣的缺点，请在评论中告诉我们。
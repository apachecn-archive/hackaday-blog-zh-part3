# 如何通过电脑控制您的仪器:这比您想象的要简单

> 原文：<https://hackaday.com/2016/11/16/how-to-control-your-instruments-from-a-computer-its-easier-than-you-think/>

曾经有一段时间，在背板上带有用于计算机控制的 GPIB 连接器(通用接口总线)的仪器是昂贵而奇特的设备，不太可能在硬件黑客的工作台上找到。你的雇主或大学可能会有，但你更有可能拥有你父母那一代熟悉的全模拟长椅。

[![A GPIB/IEEE488 plug. Alkamid [CC BY-SA 3.], via Wikimedia Commons](img/672dde90ef25d287eefa93bd0476d27b.png)](https://hackaday.com/wp-content/uploads/2016/10/a_gpib_plug.jpg) 

一个 GPIB/IEEE488 插头。Alkamid [CC BY-SA 3。]，通过[维基共享](https://commons.wikimedia.org/wiki/File:A_GPIB_plug.jpg)。

今天摆在你面前的经济实惠的仪器可能没有物理 GPIB 端口，但它们很可能有一个 USB 端口，甚至是以太网，你可以通过它进行同样的控制。制造商会提供一些软件让你使用，但是如果它不需要任何费用，如果它是好的，或者可以在微软视窗之外的平台上使用，那你就是幸运的了。

这就是你的情况，你有一个仪器，它通过一个物理接口说出一个完整记录的协议，你有足够的备用插座，但是如果你是一个 Linux 用户，特别是如果你没有 x86 处理器，你在软件方面就有点不走运了。肯定有办法让你的电脑和它说话！

让我们试一试——我将使用一台 Linux 机器和一个流行品牌的示波器，但该技术适用范围很广。

### 用签证很容易

我们很幸运，因为 National Instruments 已经制定了一个标准，将所使用的各种物理协议和接口结合在一起，并且他们的 [VISA(虚拟仪器软件架构)](https://www.ni.com/visa/)可作为 Windows 和 Linux(x86)的预编译库。与 VISA 对话是一条常见的途径，例如，如果你是一名 Python 程序员，有一个名为 py VISA 的包装器[，通过它你可以随心所欲地指挥你的乐器。如果你已经发现没有 NI VISA 库的架构的明显差距，他们也已经解决了。](https://pyvisa.readthedocs.io/en/stable/index.html) [PyVISA-py 是 VISA](https://pyvisa-py.readthedocs.io/en/latest/) 的纯 Python 实现，取代了它。

作为演示，我们将带您了解在 Raspberry Pi 上使用 PyVISA-py 和 PyVISA 通过 USB 与仪器进行基本通信的过程。我们使用了 Raspberry Pi Zero 和 Raspberry Pi 3，它们都运行最新的 Raspbian 发行版，但是类似的路径应该适用于大多数其他 Linux 环境和类似的工具。我们的仪器是 Rigol DS1054z 示波器。

我们首先为 USB、PyVISA-py 和 PyVISA 安装 Python 库。我们假设你已经有了 python 和 pip，如果没有的话[这里有一页详细介绍了它们的安装](https://www.raspberrypi.org/documentation/linux/software/python.md)。在命令提示符下键入以下几行:

`sudo pip install pyusb
sudo pip install pyvisa
sudo pip install pyvisa-py` 

现在，您应该能够从 Python 解释器测试安装了。确保仪器已打开并通过 USB 连接，然后键入以下内容:

`sudo python`

这应该会给出 Python 的版本和版权信息，然后是一个三箭头> > > Python 解释器提示。键入以下 Python 代码行:

`import visa
resources = visa.ResourceManager('@py')
resources.list_resources()`

第一行导入 VISA 库，第二行将资源管理器加载到一个变量中，第三行查询连接的仪器列表。第 2 行中的' @py '告诉资源管理器查找 PyVISA-py，如果括号为空，它将查找 NI VISA 库。

如果一切正常，您将会看到它返回您所连接的仪器的资源名称列表。如果您只有一台仪器，它应该与我们 Rigol 使用的仪器相似:

`(u'USB0::6833::1230::DS1ZA123456789::0::INSTR',)`

单引号中以 USB0::开头的部分是您的仪器的 VISA 资源名称。这是您在编写的后续代码中识别和连接它的方式，因此您需要在脚本中运行上面的 Python 代码，并在连接之前检索资源名称，或者像我们在本演示中所做的那样，从提示中复制它，并在脚本中对它进行硬编码。硬编码在任何方面都不是可移植的，因为脚本可能只适用于您的特定仪器，但是它确实提供了一种方便的方法来演示这种情况下的原理。

如果此时您仍在 Python 解释器中，您可以离开它，通过键入 control-D 文件结束字符返回到命令提示符。

### 更有用的东西

假设前面段落中的所有步骤进展顺利，现在您应该准备好编写自己的代码了。我们会给你一个简单的例子，但是首先有一些你想熟悉的文档。第一个是 PyVISA 文档，和我们之前链接的一样，第二个应该是你的仪器的编程参考。制造商的网站应提供下载，在我们的 Rigol [中，可以找到 PDF 文件](https://www.rigolna.com/products/digital-oscilloscopes/1000z/)(点击顶部的“产品手册”链接)。

PyVISA 手册详细介绍了所有包装器功能，并有一套教程，而产品手册列出了仪器支持的所有命令。在产品手册中，您可以找到复制所有界面控件和功能的命令，但我们最感兴趣的是测量(MEAS)命令集。

例如，我们将测量 Rigol 通道 1 的均方根电压。我们将使用其资源名称直接连接到仪器，并查询其型号标识符，然后选择通道 1 并查询其均方根电压读数。

将以下代码复制到文本编辑器中，用您自己的工具的标识符替换资源标识符，并将其保存为. py 文件。在我们的例子中，我们将其保存为 query_rigol.py。

```
#Bring in the VISA library
import visa
#Create a resource manager
resources = visa.ResourceManager('@py')
#Open the Rigol by name. (Change this to the string for your instrument)
oscilloscope = resources.open_resource('USB0::6833::1230::DS1ZA123456789::0::INSTR')
#Return the Rigol's ID string to tell us it's there
print(oscilloscope.query('*IDN?'))
#Select channel 1
oscilloscope.query(':MEAS:SOUR:CHAN1')
#Read the RMS voltage on that channel
fullreading = oscilloscope.query(':MEAS:ITEM? VRMS,CHAN1')
#Extract the reading from the resulting string...
readinglines = fullreading.splitlines()
# ...and convert it to a floating point value.
reading = float(readinglines[0])
#Send the reading to the terminal
print reading
#Close the connection
oscilloscope.close()

```

启用仪器上的通道——当您熟悉 API 时，您可以使用您的软件完成此操作——并将其连接到信号。我们使用示波器校准终端作为方便的方波源。然后，您可以如下运行脚本，如果一切正常，您将获得仪器 ID 字符串和电压读数:

`sudo python query_rigol.py`

值得注意的是，我们刚刚通过 sudo 命令以 root 用户身份运行 Python，以使用 USB 设备来实现本演示的目的。这超出了本页面的范围，但是你会想要查看 udev 规则以允许其作为非超级用户使用。

幸运的话，在这一页，我们将揭开控制 USB 连接仪器的神秘面纱，你应该有勇气自己尝试一下。虽然我们还没有完成，但是本文的第二部分将给出一个更完整的例子，它有一个实际的目的；我们将使用 Raspberry Pi 和 Rigol 来测量 RF 滤波器的带宽。
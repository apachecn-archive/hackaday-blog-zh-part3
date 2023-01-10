# 原子 Arduino(和其他)开发

> 原文：<https://hackaday.com/2016/04/23/atomic-arduino-and-other-development/>

即使是最铁杆的 Arduino 粉丝也不得不承认 Arduino 开发环境并不是世界上最棒的文本编辑器(他们可能会说它的简单性是它的优势，但我们现在忽略这一点)。如果你习惯于使用一个真正的代码编辑器，你可能会切换到用它编写 Arduino 代码，然后使用 IDE 中的外部编辑器集成。

这很好，但还有其他选择。我们注意到的一个是， [PlatformIO](https://hackaday.io/project/7980-platformio) ，它扩展了 GitHub 的 Atom 编辑器。这使得它可以跨平台，功能强大，并且有很多自定义插件。它还支持一系列平台，包括 Arduino、许多 ARM 平台、MSP430，甚至运行 Linux 或 Windows 的桌面计算机。

作者声称该插件将为 200 多块嵌入式电路板生成代码。它处理所有常见的开发任务，甚至包括一个终端窗口。如果你想构建脚本或者制作文件，绕过 GUI，有命令行工具。

您可以在 Windows、Linux 或 Mac 上安装 Platform.io。它使用 Python，所以将它移植到其他地方可能也很容易。特性列表很广泛:代码完成、林挺、多个项目和库管理。它甚至可以从 Arduino IDE 中导入项目。有很多插件可以添加特性(比如 Emacs 键绑定，尽管这需要一点故障排除)。

如果您经常来回切换，拥有一个针对不同平台的单一 IDE 也是有吸引力的。平心而论，Arduino IDE 并不像以前的那么糟糕，它们都在工作中有显著改进的版本( [Arduino Create](https://blog.arduino.cc/2015/05/05/sneak-peak-arduino-create/) 和 [Arduino Studio](http://labs.arduino.org/Arduino+Studio) )。在过去，我们已经看到了很多针对 Arudino 的其他 IDE 黑客。

谢谢你的提示[马丁]
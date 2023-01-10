# 同时读取 16 个旋转编码器

> 原文：<https://hackaday.com/2017/10/21/reading-16-rotary-encoders-at-the-same-time/>

我们正在挖掘这些由[fattore.saimon]构建的[菊花链编码器](https://hackaday.io/project/27611-i2c-encoder)。每个模块由一个附在 PCB 上的旋转编码器组成，PCB 背面有 PIC16F15386。正如我们过去所报道的，微芯片今年发布了他们的[功能丰富的 PIC16 微处理器](https://hackaday.com/2017/02/21/microchip-launches-new-family-of-pics/)，很高兴看到它们开始出现在项目中。每个 PCB 背面有 4 个地址跳线，[fattore.saimon]能够连接总线上多达 16 个编码器。模块也有公插头和母插头，因此他也可以物理连接它们，以简化布线。每个模块还有一个可控制的双色 LED，用于跟踪每个编码器的设置。

如果你有兴趣自己制作，你可以[从 Tindie 购买 PCBs】或者](https://www.tindie.com/products/Saimon/i2c-encoder/)[从创作者的 GitHub 下载项目文件](https://github.com/Fattoresaimon/i2cencoder)，包括一个 Arduino 库。

我们喜欢 Hackaday 网站上的编码器— [制作 DIY 编码器](https://hackaday.com/2016/01/08/video-gives-you-the-basics-of-diy-rotary-encoders/)，以及在像[这种精密切割夹具](https://hackaday.com/2017/06/04/arduino-and-encoder-form-precision-jig-for-cutting-and-drilling/)这样的项目中使用它们。一定要读一读我们的同事[Al]的[关于编码器](https://hackaday.com/2017/01/11/encoders-spin-us-right-round/)的伟大作品。
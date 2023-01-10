# 通过基准电压源提供 4 位音频输出

> 原文：<https://hackaday.com/2016/07/30/16-bit-audio-output-via-voltage-reference/>

[Bruce Land]将他的微处理器编程课程从 Atmel parts 转到了 Microchip 的 PIC32 系列，这意味着他有了一套略有不同的外围设备。然而，这两款芯片都缺少一个数模转换器(DAC)。或者他们有吗？(Dun-dun-dun-duuuuhnnnn！)

PIC 部分有一个可编程的 16 级基准电压源。如果不是经过校准的 DAC，`Vref`是什么？考虑到这一点，[Bruce]开始记录[的性能](https://hackaday.io/project/4985-pic32-vref-output-plays-wav-files)，并开始推动它远远超出制造商的意图。原来`Vref`有大约 200 kHz 的带宽。(谁会每秒更新基准电压 200，000 次？)

总之，[布鲁斯]就是[布鲁斯]，他注意到除了最低有效位，这些位不会经常改变:音频波形，采样足够快，是相当连续的。这建议使用[差分 PCM 编码](https://hackaday.io/project/273-speech-playback-for-microcontroller)，这将比特率降低了 50%，并节省了大量存储空间。(这个实验的所有代码的链接都在他的文章中。)

[布鲁斯]在康奈尔大学上的早教课的音频黑客总是一种享受。从你必须唱歌才能打开的[锁，到编程到 FPGA](http://hackaday.com/2014/12/17/singlock-protects-your-valuables-from-shy-people/) 中的 [chiptunes，各种爱好的音乐迷都可以找到。](http://hackaday.com/2016/06/19/recreating-chiptunes-in-verilog/)
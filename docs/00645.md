# 面向对象的状态机操作系统开始开源

> 原文：<https://hackaday.com/2015/11/14/object-oriented-state-machine-operating-system-goes-open-source/>

在台式计算机上，你认为操作系统是一大块复杂的软件。对于小型系统(如 Arduino)，您可能想要更简单的系统。[面向对象状态机操作系统(OOSMOS)](http://oosmos.com/) 是一个单文件和高度可移植的操作系统，它最近开始开源。

OOSMOS 有一个独特的方法，因为它是无线程的，这使得它很容易在内存受限的系统中使用，因为不存在的线程不需要堆栈。执行单元是包含状态机的 C++对象(尽管您可以使用 C)。

可以在线阅读 [API 文档](http://oosmos.com/api)。请记住，这不是像 Windows 或 Linux 那样的最终用户操作系统，而是用于管理多项任务的操作环境。不过，您可以在 Windows 或 Linux 以及许多其他主机系统下使用 OOSMOS。

为了了解可移植性选项，考虑强制的[眨眼示例](http://oosmos.com/examples/blink)。平台包括 Arduino、ESP8266、PIC32、Chipkit、Raspberry Pi 等。Arduino 代码(部分)如下所示:

```
static void SetupToggle(int Pin, int OnTimeMS, int OffTimeMS)
{
  pin * pPin = pinNew(Pin, pinOut, pinActiveHigh);
  toggleNew(pPin, OnTimeMS, OffTimeMS);
}

extern void setup()
{
  SetupToggle(13, 2000, 2000);
  SetupToggle(12, 100, 100);
  SetupToggle(11, 50, 1500);
}

extern void loop()
{
   oosmos_RunStateMachines();
}

```

SetupToggle 对象是状态机对象。setup 函数创建这个对象的三个实例，loop 函数调用 OOSMOS 主循环。SetupToggle 中使用的 [pin 类](http://oosmos.com/classes#id_The_Pin_Class_'pin')是 OOSMOS 硬件抽象的一部分，而 [toggle](http://oosmos.com/classes#id_The_Toggle_Class_'toggle') 对象本身是可重用类的一部分。

当然，像所有闪烁的 LED 例子一样，这非常简单。但是其他示例展示了同步函数和其他高级用途，包括 Windows 和 Linux 的网络代码。

在之前，我们已经讨论过简单的机器人专用操作系统[。对于](http://hackaday.com/2014/01/29/the-robot-operating-system-ros-101/)[专用的处理器](http://hackaday.com/2015/04/17/energia-multitasking-uses-rtos-on-msp432/)也有很多选择，但是 OSMOS 看起来是一个跨越广泛硬件范围的便携产品的绝佳选择。如果你想了解状态机理论中的[，我们也为你准备好了。](http://hackaday.com/2015/08/13/becoming-a-state-machine-design-mastermind/)
# 嵌入埃利奥特:中断，丑陋

> 原文：<https://hackaday.com/2015/10/02/embed-with-elliot-interrupts-the-ugly/>

欢迎来到“中断:好的、坏的和丑陋的”的第三部分。我们已经[表达了我们对中断](http://hackaday.com/2015/09/18/embed-with-elliot-interrupts-the-good/)的喜爱，展示了它们如何有助于沉着地解决多种常见的微控制器任务。那确实很好。然后我们探讨了一些可能突然出现的[调度和优先级问题](http://wp.me/pk3lN-I76)，特别是如果你的中断服务程序(ISR)运行太长时间，或者做了过多的事情。这很糟糕，但是我们可以通过编写轻量级 ISR 来解决这些问题。

无论好坏，这一期揭示了我们最不喜欢的在小型微控制器上运行中断的副作用，那就是您对代码正在做什么的假设可能是错误的，有时会带来灾难性的后果。会变得很难看的

TL；DR:一旦你开始从内部中断改变变量，你就不能再指望它们的值保持不变——你永远不知道中断什么时候会发生！墨菲定律说它会在最坏的时候发生。解决方案是暂时关闭关键代码块的中断，这样您自己的 ISR 就不能破坏您的计划。(听起来很简单，但请继续阅读！)

在这一期中，我们将从本质上讨论同一个问题的两个方面，并演示一个半解决方案。但是不用担心。到本文结束时，你应该有信心无所畏惧地编写中断，因为你将了解敌人。

## 竞赛条件

如果你还记得[我们关于`volatile`关键词](http://hackaday.com/2015/08/18/embed-with-elliot-the-volatile-keyword/)的专栏，当你想在一个 ISR 和你的代码主体之间共享数据时，你必须使用一个全局变量，因为 ISR 不能接受任何参数。因为编译器看不到全局变量在任何地方改变，我们用关键字`volatile`标记它们，告诉编译器不要优化掉这些变量。我们应该听从自己的建议:ISR 访问的变量可能会在没有通知的情况下随时改变。

与 ISR 共享变量时的“明显”陷阱是[竞争条件](https://en.wikipedia.org/wiki/Race_condition):您的代码在这里设置变量的值，然后在那里再次使用它。问题中的“竞赛”是你的代码从 A 点到 B 点是否足够快，中间是否没有中断。

让我们从一个针对 AVR 微控制器的小测验开始:

```

volatile uint16_t raw_accelerometer;
volatile enum {NO, YES} has_new_accelerometer_reading;

ISR(INT1_vector){
	raw_accelerometer = read_accelerometer_z();
	has_new_accelerometer_reading = YES;
}

...

int main(void){
	while (1){

		if (has_new_accelerometer_reading == YES){
			if (raw_accelerometer != 0){
				display(raw_accelerometer);
			}
			// Flag that we've handled this sample
			has_new_accelerometer_reading = NO;
		}
	}
}

```

显然，我们已经阅读了 Elliot 的最后一段嵌入内容，因为这里的 ISR 很少，而且只做了最少的工作。所有的逻辑和打印命令都在主循环中，不会给其他潜在的中断带来麻烦。金星！

然而，问题是我们偶尔会在显示器上看到零值。这怎么可能呢？我们只在明确测试加速度计值不为零后才显示它。

上面这句话的关键词是“之后”。考虑加速度计更新中断发生的最糟糕时间，在测试`raw_accelerometer`不为零，但在打印数值之前，情况如何？是的，这样就可以了。

当然，恰好在测试语句的最后一条指令期间触发中断的可能性相对较小。不会经常发生吧？请记住，您的代码会在`main()`循环中运行很多次，如果加速度计更新足够频繁，您可以肯定小故障*将会*发生。它只是偶尔发生，这是最难追踪和消灭的[类型的错误](https://en.wikipedia.org/wiki/Heisenbug)。

### 影子变量:一个尝试性的解决方案

这里有一个试用解决方案:

```

int main(void){
	uint16_t local_accelerometer_data = 0;
	while (1){

		if (has_new_accelerometer_reading == YES){
			local_accelerometer_data = raw_accelerometer;
			if (local_accelerometer_data != 0){
				display(local_accelerometer_data);
			}
			// Flag that we've handled this sample
			has_new_accelerometer_reading = NO;
		}
	}
}

```

看到那里发生了什么吗？我们添加了一个不与 ISR 共享的变量`local_accelerometer_data`，然后我们处理该副本，而不是 ISR 可以更改的变量。现在零值测试和`display`语句都保证基于相同的值。

这只是一半的解决方案，因为在我们处理它的本地卷影副本时,`raw_accelerometer`变量仍然可以改变。在这里，这没有问题，但是如果我们要将我们的本地副本存储回共享变量中，我们将冒这样的风险:在我们处理我们的本地副本时,`raw_accelerometer`变量已经改变，通过写回我们的本地副本，我们将覆盖刚刚改变的值。这不是小事，因为我们会丢失一个数据点，但至少在`local_accelerometer_data`上完成的工作对于我们复制它时手头的数据是正确的。

如果你正在一台豪华的 32 位整数的高级 ARM 机器上工作，这个半解决方案可能适合你。对于我们这些在 8 位机器上访问共享的 16 位变量的人来说，在我们给出所有这些的银弹解决方案之前，还有一个复杂的问题需要解决。

## 原子性和 8 位布鲁斯

原子性是不可分割的属性。(就像原子直到 20 世纪初一样。)当你用高级语言写一个单一的操作时，它*可以*最终编译成机器代码中的一个单一指令，但是更多的时候，它需要几个指令。如果这些指令会被中断，从而改变结果，那么它们就不是原子的。

坏消息是:T2 几乎没有什么东西是原子的。例如，即使像`++i;`这样简单的东西也可以翻译成三条机器指令:一条从内存中获取`i`的值到一个临时寄存器中，一条添加到寄存器中，第三条将结果写回内存中。

`++i;`中的非原子性是相当良性的，因为临时寄存器就像上面的影子变量一样工作。如果`i`在内存中被更改，当加法操作在 CPU 的寄存器中进行时，内存将被加法操作覆盖。但是至少存储回`i`T3 的值将是操作开始时的值加 1。

在 8 位机器上，处理 16 位或更长的共享变量时，可能会发生更奇怪的事情。访问 16 位变量从根本上是不同的，因为即使创建变量的影子变量版本也不是原子的，每个字节一条指令，因此是可中断的。为了看到这一点，我们需要求助于汇编语言，回想一下我们共享的 16 位`raw_accelerometer`变量的本地副本。

对于这个例子，我们使用的是`avr-gcc`，它附带了一整套工具。一个这样的工具是`avr-objdump`,它将编译好的机器代码反汇编成“可读”的汇编语言。具体来说，如果您已经使用调试标志(`-g`)编译了代码，那么类似于`avr-objdump -S myCode.elf > myCode.lst`的输出会返回您的原始代码，其中夹杂着汇编语言版本的代码。

```

     local_accelerometer_data = raw_accelerometer;
b8:	80 91 00 01 	lds	r24, 0x0100
bc:	90 91 01 01 	lds	r25, 0x0101

```

无论如何，你不必是汇编语言大师，也能看出我们所认为的一个操作需要两条不同的汇编语言指令。第一条指令将`raw_accelerometer`数据的低八位复制到`r24`工作寄存器中，第二条指令将高八位复制到工作寄存器中。

现在，ISR 可以打击并改变我们的共享`raw_accelerometer`价值的最糟糕的地方在哪里？在两个`lds`指令之间。当变量访问或操作需要一条以上的机器/汇编指令时，原子性的失败和可怕的小故障还有可能，这些都是由 ISR 共享的变量引起的。特别是，这打破了我们以前对原子性问题的“解决方案”。

注意这有多难看。当中断在两个`lds`命令之间命中时，变量的副本包括一个读数的低位和一个完全不同值的高位。这是两个值的混合，一个本来就不存在的数字。每当您使用与 ISR 共享的 16 位变量时，都会出现这种情况。

我们已经编写了[一些示例代码来为您演示这一现象](https://github.com/hexagon5un/avr_atomic_demo.git)。它可以在任何 AVR 微控制器上运行，包括基于 AVR 的 Arduino。每次发现损坏的值时，代码都会闪烁 LED，最终看起来像一个萤火虫约定，即使我们已经将中断速度降低到每 65，536 个 CPU 周期一次中断。我们需要解决这个问题！

### 抛开 Arduino 不谈

上述原子性最糟糕的失败是由于在 8 位机器上与 ISR 共享 16 位变量造成的。如果我们只需要从加速度计中读取 8 位，那么“影子变量”解决方案就能很好地工作。我们在这里重申这一点，因为我们看到在 Arduino 代码中使用了很多 16 位的`int`,而更短的数据类型就足够了。

我们并没有责怪 Arduino 用户——大多数内置的 Arduino 示例代码都使用`int`来处理任何事情，包括 pin 码。AVR Arduino 上的 16 位`int`的范围从-32，768 到 32，767。当 Arduinos 拥有超过 255 个 pin 时，这可能是很好的未来保障，但我们无法想象需要访问 pin 号-32，000，无论这意味着什么。我们认为，对所有事情都使用`int`背后的基本原理是，学习不同的数据类型很困难。

如果只是浪费 RAM 或 CPU 周期的问题，那就没问题了。但是默认使用`int` s 意味着你在不知道的情况下将各种非原子性引入到你的代码中。正如你在这里看到的，一旦你在混合中加入中断，它就是一个灾难的配方:不要在 8 位机器上使用 16 位数字，除非你需要。

那么 Arduino 是如何工作的呢？这些库(大部分)不再是以这种草率/幼稚的方式编写的了。事实上，一旦我们一劳永逸地解决了原子性的问题，我们就会拆开`millis()`函数。你会发现它做了完全正确的事情。

## 最后，真正的原子性

重新概括一下:与 ISR 共享的变量可能会在没有通知的情况下发生变化，而创建变量的本地副本只能解决一半问题，因为本地副本只有在创建副本的操作是原子操作时才起作用。当我们不看的时候，我们如何确保中断不会改变我们的变量？答案非常简单:关闭中断。

事实上，如果我们愿意再次打开和关闭中断，我们甚至根本不需要担心创建影子局部变量。

```

int main(void){
	while (1){

		if (has_new_accelerometer_reading == YES){

			cli();  // clears the global interrupt flag

			if (raw_accelerometer != 0){
				display(raw_accelerometer);
			}
			// Flag that we've handled this sample
			has_new_accelerometer_reading = NO;

			sei();  // re-enables interrupts
		}
	}
}

```

很简单，而且有效。见鬼，在 AVR 上，中断禁用/启用命令直接翻译成机器代码，每个只需要一个周期。很难打破这个记录。除非你禁用中断相当长的时间。

但是我们可以使用局部变量复制技巧:

```

int main(void){
	uint16_t local_accelerometer_data = 0;
	while (1){
		if (has_new_accelerometer_reading == YES){

			cli();  // clears the global interrupt flag
			local_accelerometer_data = raw_accelerometer;
			sei();  // re-enables interrupts

			if (local_accelerometer_data != 0){
				display(local_accelerometer_data);
			}
			// Flag that we've handled this sample
			has_new_accelerometer_reading = NO;
		}
	}
}

```

现在只需要保护局部变量的赋值，所以中断只在几个周期内不起作用。太棒了。(同样，记住关于底层“原始”数据与本地副本不同步的警告。)

### 阿尔杜伊诺毫

我们上面的代码没有做的一件事是首先检查中断是否被设置。我们简单地假设中断是打开的，并且在我们完成我们的临界区之后，将它们重新打开。但是如果它们一开始就没有打开，那么我们就无意中改变了一些东西。解决方案是记录包含全局中断使能位的状态寄存器`SREG`的值，并在临界区结束后将其恢复。

正如所承诺的，这是来自 Arduino 库的毫秒计数器例程。(有兴趣的话在“wiring.c”里。)

```

unsigned long millis()
{
        unsigned long m;
        uint8_t oldSREG = SREG;

        // disable interrupts while we read timer0_millis or we might get an
        // inconsistent value (e.g. in the middle of a write to timer0_millis)
        cli();
        m = timer0_millis;
        SREG = oldSREG;

        return m;
}

```

请注意，它只为正确的原因做正确的事情——这就是 Arduino 计时器代码实际工作的原因。首先，它复制包含旧的全局中断使能位的`SREG`的值。然后，它创建当前(ISR 共享的)毫秒计数器的本地副本。最后，它恢复`SREG`并返回毫秒数。干得好。

### 原子块

为保护像这样的关键部分制定一个通用的解决方案变得有点棘手。至少，我们会像在`millis()`中一样复制`SREG`的内容。AVR 库有一个“util/atomic.h”头文件，它定义了基本上为我们做这件事的`ATOMIC_BLOCK`包装器。

有两个可能的参数，`ATOMIC_RESTORESTATE`和`ATOMIC_FORCEON`，它们分别对应于两种情况:程序块首先判断全局中断向量是否预先打开，或者只是假设它是打开的，并在最后将其设置为打开。

而且`ATOMIC_BLOCK`实际上比我们目前讨论的更聪明。它包括一个代码技巧，允许您在块内使用`return`或`break`语句，并且它仍然会为您重新设置全局中断标志。

作为一个例子，这里是 Arduino 的`millis()`重写，以利用标准的 GCC AVR 库:

```

unsigned long millis(){
    ATOMIC_BLOCK(ATOMIC_RESTORESTATE){
	    return timer0_millis;
    }
}

```

据我们估计，这比原来的要清楚得多。使用`ATOMIC_BLOCK`为您省去许多麻烦，并使代码更容易读取。事实上，如果您想节省调用开销，您可以简单地从主例程中自己使用`timer0_millis`，只要您将它包装在一个`ATOMIC_BLOCK`中:

```

ATOMIC_BLOCK(ATOMIC_RESTORESTATE){
    if (timer0_millis &gt; alarm_time){
        do_whatever();
    }
}

```

### 最后可能的改进

如果您是那些优化程序类型的人之一，您会注意到只有一个特定的 ISR 与临界区共享我们的变量。除了禁用所有中断，您还可以想象只禁用导致问题的特定中断。

这也会让我们获得原子性，除了代码复杂，我们想不出任何理由不这样做。这意味着放弃一刀切`ATOMIC_BLOCK`式的全局中断操作，但如果您对其他不想阻塞的中断有实时约束，这可能是值得的。尽管如此，我们在实践中已经看到了很多全局中断禁用。有读者愿意提供一些现实世界中的例子吗？在这些例子中，只有特定的中断被禁用，以保护一个关键的原子部分。

## 结论

这是一次关于中断主题的史诗之旅，我们希望你喜欢。中断是微控制器武库中最强大的工具，因为它们直接回答了微控制器应用的头号问题:与现实世界的外设接口。掌握中断会让你从一个微控制器初学者完全进入中级阵营，所以这是值得的。

中断还引入了一定程度的多任务处理，随之带来了诸如调度和优先级(不好的)、原子性故障和竞争条件(不好的)等问题。了解这些问题是成功的一半。使用中断还会有其他我们忽略的大陷阱吗？你最喜欢的打断恐怖故事有哪些？请在评论中发表。
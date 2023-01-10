# 代码工艺-嵌入 C++:破解 Arduino 软件环境

> 原文：<https://hackaday.com/2015/12/31/code-craft-embedding-c-hacking-the-arduino-software-environment/>

Arduino 软件环境，包括 IDE、库和通用方法，都是面向教育的。这是向新手介绍嵌入式开发的一种方式。这是一个伟大的概念，但当需要更严肃的发展或更先进的教育时，它就不够了。我一直在纠结如何解决这个问题。一种方法是使用带有 Arduino 插件的 [Eclipse。这至少提供了一个专业的开发环境。](http://hackaday.com/2015/10/30/code-craft-using-eclipse-for-arduino-development/)

Arduino 的代码库是另一个挫折。坦率地说，`setup()`和`loop()`的使用和`main()`的隐藏真的让我很烦。库和示例中 C 和 C++的混合是另一个令人恼火的地方。有足够多的 C++被使用，它应该成为标准是有意义的。另外，很大一部分库代码可以做得更好。在这一点上，解决这个问题将是一个巨大的任务，需要许多专门的开发人员来重写。但是有些事情是可以做到的，所以让我们来看看几种可能性以及如何使用它们。

# *主*黑客

如前所述，隐藏`main()`让我烦恼。它是 C++固有的一部分，这使得它对于学习这门语言非常重要。到目前为止，我还没有考虑如何解决这个问题。我从代码库中了解到 Arduino `main()`的存在——它必须存在，因为这是 C++标准所要求的。我灵光一现，尝试将文件`main.cpp`中的代码复制到我自己的代码中。它构建了，但是我如何确定它使用的是我的代码，而不是 Arduino 库中的原始代码？我注释掉了`setup()`,它仍然在构建，所以它必须使用我的版本，否则就会出现关于`setup()`丢失的错误。你可能会奇怪它为什么用我的版本。

当你构建一个程序时…是的，它是一个“程序”而不是“草图”，是一个“子板”而不是“屏蔽”，是一个“链接器”而不是一个“组合器”！为什么每个人都试图改变软件开发使用的语言？

当你构建一个 C++程序时，有两个主要阶段。使用编译器编译代码。这会生成许多目标文件——每个源文件一个。链接器然后组合编译后的对象来创建可执行文件。链接器从寻找 C 运行时代码(CRTC)开始。这是在调用`main()`之前做一些设置的代码。在 CRTC 中会有外部符号，`main()`是其中之一，其代码存在于其他文件中。

链接器将在两个地方寻找那些丢失的符号。首先，它加载所有的目标文件，从它们中挑选出符号，并建立一个缺失的列表。其次，它在所有包含的预编译对象库中查找剩余的符号。如果仍然缺少任何符号，它将发出一条错误消息。

如果你查看 Arduino 文件，你会发现一个包含一个`main()`函数的`main.cpp`文件。最后被放在图书馆里。当链接器启动时，我的`main()`版本在一个新创建的目标文件中。因为首先处理目标文件，所以链接器使用我的版本`main()`。库版本被忽略。

`main()`还是有些不寻常。下面是`main()`中的无限`for`循环:

```

	for (;;) {
		loop();
		if (serialEventRun) serialEventRun();
	}

```

对`loop()`的调用是预期的，但是为什么会有`if`语句和`serialEventRun`？该函数检查串行输入数据是否可用。`if`依赖于工具链的一个技巧，而不是 C++，它检查符号`serialEventRun`的存在。当符号不存在时，省略`if`及其代码。

## 切换*设置()*和*循环()*

现在我可以控制`main()`了，我可以解决我的另一个讨厌的问题了，那就是`setup()`和`loop()`函数。我可以通过创建自己版本的`main()`来消除这两个函数。我并不是说使用`setup()`和`loop()`是错误的，尤其是考虑到 Arduino 的教育目标。使用它们可以清楚地了解如何组织一个嵌入式系统。这是 C++构造函数和成员函数背后的相同概念。在正确的时间和地点完成初始化，一大堆软件问题就烟消云散了。但是由于 C++通过类自动提供了这一点，下一步就是利用 C++的能力。

## 全局实例化

C++的一个问题是全局或文件范围类实例的初始化成本。正如我们在介绍类的文章[中看到的，在`main()`之前执行了一些额外的代码来处理这个问题。我认为这个开销足够小，所以不成问题。](http://hackaday.com/2015/11/06/code-craft-embedding-c-classes/)

初始化的顺序可能是一个问题。顺序是在一个编译单元(通常是一个文件)中从第一个声明到最后一个声明定义的。但是在编译单元之间，顺序是不确定的。一次，文件 A 中的所有全局变量可能首先被初始化，而下一次，文件 B 中的全局变量可能首先被初始化。当一个类依赖于另一个首先被初始化的类时，顺序是很重要的。如果它们在不同的编译单元中，这是不可能保证的。一种解决方案是将所有的全局变量放在一个编译单元中。如果库包含全局实例，这可能不起作用。

一个相关的问题发生在大型嵌入式计算机系统上，比如运行 Linux 的 Raspberry Pi，当来自命令行的参数被传递给`main()`时。环境变量也是一个问题，因为它们可能直到`main()`执行后才可用。全局实例将无法访问此信息，因此在初始化期间无法使用它。我遇到了这个问题，我的机器人的控制计算机是一台个人电脑。我用机器人的网络名来决定它们最初的行为。在输入`main()`之前它是不可用的，所以它不能用于初始化全局实例。

这是小型嵌入式系统的一个问题，它们不传递参数或者没有环境值，但是我不想只关注它们。我希望解决包括大型系统在内的一般情况，所以我们假设不需要全局实例。

# *程序*类

我正在采取并与你分享的方法是一个实验。我过去在一个机器人项目中做过类似的事情，但是这种方法没有被彻底分析。正如经常发生的那样，我没有时间了，所以我实现了这个快速解决方案。从长远来看，这是否有用，我们还得看看。如果没有别的，它将向你展示更多关于 C++的工作。

我的方法是创建一个带有成员`run()`函数的`Program`类。整个程序的设置发生在类构造函数中，而`run()`函数处理所有的处理。通常的全局变量是数据成员。

下面是一个骨架`Program`类的声明和`run():`的实现

```

class Program {
public:
	void run();
	static Program&amp; makeProgram() {
		static Program p;
		return p;
	}

private:
	Program() { }
	void checkSerialInput();
};

void Program::run() {
	for (;;) {
		// program code here
		checkSerialInput();
	}
}

```

我们只希望有一个`Program`的实例存在，所以我通过将构造函数私有并提供静态`makeProgram()`函数来返回第一次调用`makeProgram()`时创建的静态实例来确保这一点。如上所述，`Program`成员函数`checkSerialInput()`处理串行输入的检查。在`checkSerialInput()`中，如果程序没有使用串行输入，我引入了一个`#if`块来消除实际代码。

以下是`main.cpp`中`Program`的用法:

```

void arduino_init() {
	init();
	initVariant();
}

int main(void) {
	arduino_init();
	Program&amp; p = Program::makeProgram();
	p.run();
	return 0;
}

```

函数`initArduino()`是内联的，它处理设置 Arduino 环境所需的两个初始化例程。

优秀软件开发的技术之一是隐藏复杂性，并为其功能提供一个描述性的名称。这些函数不仅隐藏了代码，而且在某种情况下还隐藏了条件编译。

# Redbot 线追随者项目

这个代码实验使用 Sparkfun Redbot 设置进行行跟踪。这是一个两轮机器人，有 3 个光学传感器来检测线路，还有一个 I2C 加速度计来检测物体的碰撞。这台电脑是一个 Sparkfun Redbot 主板，它与 Arduino Uno 兼容，但提供了一个非常不同的布局，并包括一个电机驱动器 IC。

这个机器人足够简单，可以制作一个可管理的项目，但也足够复杂，可以作为一个很好的测试，特别是当项目涉及到控制系统软件时。处理这些电机和传感器的基本代码来自 Sparkfun，只使用基本的 pin 级 Arduino 例程。我不可能破解整个 Arduino 代码，但是使用 Sparkfun 代码提供了一个易于管理的子集来进行实验。

在这篇文章中，我们将只看控制电机。让我们从测试电机例程的`Program`类的声明开始:

```

class Program {
public:
	void run();
	static Program&amp; makeProgram() {
		static Program p;
		return p;
	}

private:
	Program() { }
	static constexpr int delay_time { 2000 };

	rm::Motor l_motor { l_motor_forward, l_motor_reverse, l_motor_pwm };
	rm::Motor r_motor { r_motor_forward, r_motor_reverse, r_motor_pwm };
	rm::Wheels wheels { l_motor, r_motor };

	void checkSerialInput();
};

```

有一个名称空间`rm`包含了我为项目定义的类，因此类名前面有`rm::`。第 11 行是你可能没见过的东西，一个在 C++ 11 中新增并在 C++14 中扩展的`constexpr` 。它声明`delay_time`是在编译过程中使用的真常量，在运行时不会被分配存储空间。`constexpr`还有很多，我们将来会看到更多。我在这个项目中使用它的另一个地方是定义使用什么样的引脚。这里有一个例子:

```

constexpr int l_motor_forward = 2;
constexpr int l_motor_reverse = 4;
constexpr int l_motor_pwm = 5;
constexpr int r_motor_pwm = 6;
constexpr int r_motor_forward = 7;
constexpr int r_motor_reverse = 8;

```

`Motor`类控制一个电机。它需要两个引脚来控制方向，一个脉冲宽度调制(PWM)引脚来控制速度。引脚通过构造函数传递，名称应该是不言自明的。`Wheels`类使用`Motor`实例提供机器人的协调运动。`Motor`实例作为引用传递给`Wheels`使用。下面是两个类声明:

```

class Motor : public Device {
public:
	Motor(const int forward, const int reverse, const int pwm);

	void coast();
	void drive(const int speed);

	int speed() const {
		return mSpeed;
	}

private:
	void speed(const int speed);

	PinOut mForward;
	PinOut mReverse;
	PinOut mPwm;
	int mSpeed { };
};

class Wheels {
public:
	Wheels(Motor&amp; left, Motor&amp; right) :
			mLeft(left), mRight(right) {
	}

	void move(const int speed) {
		drive(speed, speed);
	}
	void pivot(const int speed) {
		drive(speed, -speed);
	}
	void stop() {
		mLeft.coast();
		mRight.coast();
	}

	void drive(const int left, const int right) {
		mLeft.drive(left);
		mRight.drive(right);
	}

private:
	Motor&amp; mLeft;
	Motor&amp; mRight;
};

```

`Wheels`的主力是函数`drive()`，它只是为每个电机调用`Motor drive()`函数。除了`stop()`，其他的`Wheels`功能都是使用`drive()`的实用程序，只是让开发者的工作变得更容易。编译器应该将它们转换成对`driver()`的直接调用，因为它们在类声明中是内联的。这是使用内联函数来增强类的实用性的一种有趣的方式，而不会产生任何代码或时间成本。

`Program`中的`run()`方法通过先在一个方向`pivot()`测试电机，然后以不同的速度测试另一个方向。一个`pivot()`旋转机器人到位。一旦速度被设定，它会一直持续到改变，所以`delay`功能只是给机器人提供一点时间转弯。代码如下:

```

void Program::run() {
	for (;;) {
		wheels.pivot(50);
		delay (delay_time);

		wheels.pivot(-100);
		delay(delay_time);

		checkSerialInput();
		if (serialEventRun) {
		}
	}
}

```

# 包裹

Redbot 项目是展示代码技术的有趣工具。电机程序的当前测试演示了如何覆盖现有的 Arduino `main()`。即使你不喜欢我用`Program`的方法，使用你自己的`main()`的灵活性可能对你自己的项目有用。下一篇文章将使用模板重新审视这个程序。

# 嵌入 C++项目

在 Hackaday.io，我创建了一个嵌入 C++的项目。项目将在项目描述中以目录的形式保留这些文章的列表。每篇文章都将有一个项目日志条目用于额外的讨论。感兴趣的人可以更深入地研究主题，提出问题，并分享更多的发现。

该项目也将作为我或合作者补充材料的地方。例如，有人可能想要获取代码并报告其他 Arduino 板甚至其他嵌入式系统的结果。停下来看看发生了什么事。
# C++中的感知器

> 原文：<https://hackaday.com/2016/11/08/perceptrons-in-c/>

[上次](http://hackaday.com/2016/11/02/machine-learning-foundations/)，我谈到了一种简单的叫做感知机的神经网络，你可以让它学习简单的功能。为了进行试验，我用 Excel 编写了一个简单的例子。这对于动态修改很方便，但对于将代码放入微控制器就不那么方便了。这一次，我将向您展示 C++中的代码，并告诉您在面对更复杂的问题时可以做些什么。

我构建了一个通用基类，它实现了核心逻辑，可以处理不同的向量大小。这是标题:

```
class Learn
{
protected:
 unsigned int stimct; // number of stimulus (will be +1 due to bias)
 unsigned int resct; // number of results
 float threshold; // threshold (default 1.0)
 float **weights; // weight matrix
 float *result; // results
 float *_stim; // place to put stim + bias
 void set_stim(float *s); // helper to load stim+bias
public:
 // Note: stimulusct is your stimulus count;
 // The code will add one to it to account for bias
 Learn(unsigned int stimulusct, unsigned int resultct);
 ~Learn();
 int init(void); // reset weights and threshold
 // perform training (stimulus should give result and use a training rate)
 int train(float *stim, unsigned int result, float wt=1.0f);
 // Get result for given stimulus
 unsigned int fetch(float *stim);
 // set/get threshold value
 void setThreshold(float t) { threshold=t; };
 float getThreshold(void) { return threshold; };
 // load weights from file
 int load(const char *fn);
 // save weights to file
 int save(const char *fn);
 // debug output
 void dump(void);
};
```

该类处理添加偏差输入，并为训练和分类做所有的数学计算。你可以在 [Github](https://github.com/wd5gnr/perceptron) 上找到类代码，以及一个名为 simple.cpp 的简单演示。只需运行 make 来构建示例程序。

这个简单的演示程序有一组用于 AND 逻辑的训练数据和另一组用于 or 逻辑的训练数据。以下是和数据:

```
float and_trng[4][2] = {
 { 0.0, 0.0},
 { 0.0, 1.0 },
 { 1.0, 0.0 },
 { 1.0, 1.0}
};

int and_trngr[]={ 0, 0, 0, 1 };
```

代码重复进行训练，直到出现正确的答案:

```
 for (i=0;i<4;i++) lobj.train(trainingdata[i],trainresult[i],TRAINRATE);
 for (i=0;i<4;i++) if ((res=lobj.fetch(trainingdata[i]))!=trainresult[i]) again=1;
```

再次变量导致训练/测试序列重复。如果数据不是线性可分的(例如，尝试更改数据以进行 XOR 运算)，代码将在 500 次遍历训练数据后爆发。

## 不太激动人心

当然，“与”和“或”门并不令人兴奋。要做任何真正有趣的事情，你需要[多层感知器](https://en.wikipedia.org/wiki/Multilayer_perceptron)组成一个真正的神经网络。根据数学，三层感知器足以处理任何情况。一层接受输入。该层的输出提供给“隐藏”层。这些输出馈入一层输出感知器。

当然，训练这样的网络更加困难。但是，原理是一样的。使用学习算法将输出中的误差反向传播到感知器。

## 开源和硬件

我想写一些基本的软件来说明这些原理。然而，如果你想真正提升，你可能应该求助于一个开发良好的库，比如 [OpenNN](http://www.opennn.net/) (你可以在[看到一个类似的例子](https://github.com/Artelnics/OpenNN/blob/master/examples/logical_operations/main.cpp)，它甚至包括 XOR)。或者你可以考虑 [FANN](http://leenissen.dk/fann/wp/) ，如果你不喜欢 OpenNN 的话。

如果你想在硬件中尝试一些东西，这些算法在 FPGA 中并不难实现。或者你可以[买一些硬件](http://www.general-vision.com/products/braincard/)(你可以在下面看到关于那张卡的视频)。

如果你想看一些我们已经看过的使用神经网络的项目，你可以阅读关于[瞄准猫](https://hackaday.com/2016/07/08/neural-network-targets-cats-with-a-sprinkler-system/)，玩[超级马里奥](https://hackaday.com/2015/06/14/neural-networks-and-mario/)，或者[控制直升机](https://hackaday.com/2014/04/22/self-learning-helicopter-uses-neural-network/)的内容。

 [https://www.youtube.com/embed/2SE4bnAnfMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2SE4bnAnfMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


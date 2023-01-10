# 浏览器中的张量流

> 原文：<https://hackaday.com/2018/04/16/tensorflow-in-your-browser/>

如果你想探索机器学习，你现在可以使用 JavaScript 编写应用程序，在你的浏览器中训练和部署 [TensorFlow。我们知道你在想什么。那一定很慢。令人惊讶的是，事实并非如此，因为这些库使用了图形处理单元(GPU)加速。当然，前提是你的浏览器可以使用你的 GPU。有几个可用的演示，包括一个你训练一个吃豆人游戏来响应你的网络摄像头中的手势来控制游戏。如果你尝试它，然后在你的浏览器选项中禁用加速图形，你会看到你可以从 GPU 获得多大的加速。](https://js.tensorflow.org/)

## 开始使用

文档和教程可以帮助您开始。不过，以其最简单的形式，做简单的事情是相当容易的。为了让你开始，我们把一些非常简单的东西放在一起:一个学习如何估计某个数的十倍等于多少的网络。这不是最令人惊奇的演示，但是如果你通过阅读代码来学习，这是一个开始。

流程非常简单。首先，我们从内容交付服务器加载库:

```
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@0.6.1">
```

正如你可能从名字中猜到的，张量流中的一切都是张量。我们在两个张量中创建一些训练数据，每个张量有五个元素，只有一个维度:

```
// learn 10x table
 const xs = tf.tensor2d([1,2,3,4,5], [5,1]);
 const ys = tf.tensor2d([10,20,30,40,50], [5,1]);
```

你可能猜到 xs 张量是输入，ys 张量是期望输出。

有几种模型和方法可以用来构建和训练网络。我们只是选择了一个简单的线性回归:

```
// linear regression model
 model.add(tf.layers.dense({units: 1, inputShape: [1]}));
 // Prep for training
 model.compile({loss: 'meanSquaredError', optimizer: 'sgd'});

// train -- the higher the number the more accurate you'll get (but longer run time)
 tfinterface=model.fit(xs,ys,{epochs: nr_epochs});
 }
```

## 承诺，承诺

因为这是 JavaScript，所以并行执行是通过“承诺”来处理的 promise 本质上是一个函数，当它需要作为参数的数据变得可用时，就应该运行这个函数。当输入到达时，将执行“then”中的代码。这里有一个例子:

```
// wrapper around model predict
function predict(n) {
  return tfinterface.then( () => { return model.predict(tf.tensor2d([n],[1,1])); });
}
```

这意味着当拟合完成时(`model.fit`返回一个承诺)，代码将运行`predict`方法来猜测输入`n`的结果。如果你想了解更多关于承诺的信息，谷歌[有一个很好的介绍](https://developers.google.com/web/fundamentals/primers/promises)以及对[新`await`关键词](https://developers.google.com/web/fundamentals/primers/async-functions)的相关讨论。

剩下的都是普通的 HTML 表单。你可以从 [GitHub](https://github.com/wd5gnr/tensorflowjsdemo) 获得整个文件。把它放在某个地方，然后用浏览器指向该文件。你会注意到结果并不精确，因为这是一个估计，但你做的训练越多，他们就会越好。

## 下一步是什么？

如果你想认真的话，这个网站有一些更有趣的演示。我们已经对 TensorFlow 有了自己的[介绍。虽然它不是 JavaScript，但我们确实喜欢这个](https://hackaday.com/2017/04/11/introduction-to-tensorflow/) [Python TensorFlow 教程](https://hackaday.com/2017/11/25/tensorflow-tutorial-uses-python/)。还有一个来自 TensorFlow Dev 峰会的最新视频，你可以在下面观看。

 [https://www.youtube.com/embed/YB-kfeNIPCE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YB-kfeNIPCE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)


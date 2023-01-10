# 用 150 行 Python 实现简单的量子计算

> 原文：<https://hackaday.com/2018/04/10/simple-quantum-computing-in-150-lines-of-python/>

建造一台量子计算机需要什么？许多奇异的超酷硬件。然而，创建一个模拟器并不困难，并且可以让你深入了解这种计算是如何工作的。模拟器甚至不需要很复杂。这里有一个存在于大约 [150 行 Python 代码](https://github.com/adamisntdead/QuSimPy)中的。

你可能想知道值是多少。毕竟，有很多做得很好的模拟器，包括我们过去看过的 [Quirk](https://hackaday.com/2018/01/24/quantum-weirdness-in-your-browser/) 。这个模拟器的迷人之处在于，仅用 150 行代码，您就可以一口气合理地阅读全部内容，并了解不同的操作如何真正影响状态。

需要注意的一点是，引用的 150 行代码包含注释，因此实际的代码量更少。程序的大部分处理量子寄存器和一种将矩阵应用于量子态的通用方法。这使得大多数运算只是矩阵的简单定义。例如:

```

 # Hadamard Gate
 'H': np.multiply(1\. / np.sqrt(2), np.matrix([
 [1, 1],
 [1, -1]
 ])),

```

使用模拟器需要编写更多的 Python 代码，所以这实际上是一个库，而不是像 Quirk 这样的模拟器。例如，以下是包含的部分示例代码:

```

#############################################
# Swap 2 Qubits #
#############################################
# Here, We Will Apply a Pauli-X Gate / NOT Gate
# To the first qubit, and then after the algorithm,
# it will be swapped to the second qubit.

Swap = QuantumRegister(2) # New Quantum Register of 2 qubits
Swap.applyGate('X', 1) # Apply The NOT Gate. If Measured Now, it should be 10

# Start the swap algorithm
Swap.applyGate('CNOT', 1, 2)
Swap.applyGate('H', 1)
Swap.applyGate('H', 2)
Swap.applyGate('CNOT', 1, 2)
Swap.applyGate('H', 1)
Swap.applyGate('H', 2)
Swap.applyGate('CNOT', 1, 2)
# End the swap algorithm

print('SWAP: |' + Swap.measure() + '&amp;gt;') # Measure the State, Should be 01

```

如果你想了解更多关于量子计算的知识，我们最近做了一个系列，从简单的开始[，看看](https://hackaday.com/2018/01/24/quantum-weirdness-in-your-browser/)[通信](https://hackaday.com/2018/01/31/quantum-communications-in-your-browser/)，最后看看[格罗弗的算法](https://hackaday.com/2018/02/07/quantum-searching-in-your-browser/)。
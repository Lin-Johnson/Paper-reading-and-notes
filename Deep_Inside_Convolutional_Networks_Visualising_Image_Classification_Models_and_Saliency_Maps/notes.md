## What Does Interpretability Mean?

Generally speaking, interpretability refers to the extent of human‘s ability to understand and reason a model.

- **Simulatability is considered as the understanding over the entire model.**

  模型越简单，模型越容易解释，模型的可解释性越高。

- **Decomposability is to understand a model in terms of its components, such as neurons, layers, blocks, and so on.**

  将复杂的神经网络分解为多个模块，分析各个模块的功能和可解释性。

- **Algorithmic transparency is to understand the training process and dynamics of a model.** 

  神经网络缺乏透明度体现为：

  - 算法不可解释
  - 训练数据集缺乏可视性（数据来源、数据处理、训练模型的特征）
  - 数据选择方式不透明
  - 对训练数据集中偏见的理解有限
  - 模型版本化的透明度有限

  

  

## Why Is Interpretability Difficult?

**Human Limitation** 

Expertise is often insufficient in many applications. Nowadays, deep learning has been extensively used in tackling intricate problems, which even professionals are unable to comprehend adequately.

简单来说就是没有人知道结果是怎么来的

**Commercial Barrier** 

First and foremost, companies profit from black-box models. It is not a common practice that a company makes capital out of totally transparent models. Second, model opacity helps protect hard work from being reverse engineered. An effective black box is ideal in the sense that customers being served can obtain satisfactory results while competitors are not able to steal their intellectual properties easily. Third, prototyping an interpretable model may cost too much in terms of financial, computational, and other resources. 

我不太清楚为什么要扯上商业去，他给出的解释为：

- 公司从不可解释的模型中获利，但是不会用完全透明的模式来生产资本
- 模型的不透明度有利于保护工作使得竞争对手不容易窃取到知识产权
- 构建一个可解释模型在财务、计算和其他资源方面花费太高，不值得

**Data Wildness** 

- On the one hand, although it is a big data era, high-quality data are often not accessible in many domains. 

  **高度异质性**和**不一致**的数据阻碍了深度学习模型的准确性的同时而也阻碍了可解释性的构建。

- On the other hand, real-world data have the character of high dimensionality, which suppresses reasoning.

  神经网络训练模型过程中存在维度映射，深度学习模型输入变量的数量过大。

***Algorithmic Complexity*** 

Deep learning is a kind of large scale and highly nonlinear algorithms. Convolution, pooling, nonlinear activation, shortcut, and so on contribute to the variability of neural networks. 

深度学习是一种大尺度的高度非线性算法。卷积、池化、非线性激活、快捷方式等都有助于促进神经网络的可变性。**深度学习的算法和参数的调节都会引起神经网络可解释性的改变。**

Recursiveness is another source of difficulty.

递归性是困难的另一个来源，**初始输入的微小变化可能会导致巨大的结果差异**，从而增加了解释方法的复杂性。





## How to Build Good Interpretation Method?
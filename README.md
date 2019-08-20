Udacity Machine Learning 
==============

优达学城[机器学习入门](<https://cn.udacity.com/course/intro-to-machine-learning--ud120-enterprise>)课程项目记录。课程 Github地址 [ud120-projects](<https://github.com/udacity/ud120-projects>)

# 机器学习入门

- 第01课：机器学习入门及 Sebastian Thrun 介绍，了解机器学习的在科技领域的应用。
- 第02课：[朴素贝叶斯](./naive_bayes)，在 Python 中使用 Scikit-learn 运行一个朴素贝叶斯分类器，分离训练集和测试集的机器学习数据，计算后验概率和先验概率的简单分布。
- 第03课：[支持向量机（SVM）](./svm)，学习支持向量机（SVM）背后的原理，在机器学习中实现一个 SVN 分类器，确定如何为 SVM 选择正确的内核，并学习 RBF 和线性内核。
- 课04课：[决策树](./decision_tree)，用 Python 编写简单的决策树，学习决策树算法的工作原理，包括熵和信息增益的公式以及其计算。实践一个识别邮件作者的迷你项目。
- 第05课：[选择自己的算法](./choose_your_own)，在这个迷你项目中，您将通过选择自己的算法来扩展算法工具箱，对地形数据进行分类，包括 K-Means，AdaBoost 和 Random Forest。选择最优化算法。
- 第06课：[数据集与问题](./datasets_questions)，应用机器学习知识，寻找 Enron 邮件数据集中的规律。调查美国历史上最大的诈骗案之一。
- 第07课：[回归](./regression)，了解持续监督学习与离散学习的不同，在 Python 中使用 Scikit-learn 编写线性回归代码，理解不同的错误度量，如线性回归的背景下的 SSE（最小绝对误差） 和 R 平方。
- 第08课：[异常值](./outliers)，讨论如何选择和移除异常值以提高线性回归预测的质量，在真实数据集中，移除残差并重新实现回归，在 Enron 电子邮件语料库中，应用对异常值和残差的理解。
- 第09课：[聚类](./k_means)，区分无监督学习和监督学习，使用 Python 实现 K-Means 算法，用机器学习找到聚类的中心。
- 第10课：[特征缩放](./k_means)，了解哪些算法在使用前需要首先进行特征缩放。了解如何使用特性扩展来预处理数据以改进算法，在 Scikit-learn 中使用 Min Max Scaler。
- 第11课：[文本学习](./text_learning)，学习如何在机器学习算法中使用文本数据。
- 第12课：[特征选择](./feature_selection)，讨论在什么时候以及为什么使用特征选择，并提供了一些实现此目的的技巧。学习正则化、偏差、方差。使用单变量特征选择工具 SelectKBest 选择k个最高分特征。
- 第13课：[主成分分析（PCA）](./pca)，通过主成分分析（PCA）学习数据维度和减少维度数量。分析 Scikit-learn 示例中的人脸识别项目。
- 第14课：[交叉验证](./validation)，了解有关测试，训练，交叉验证和参数网格搜索。学习 Scikit-learn 中的 GridSearchCV 进行 K 折交叉验证。使用 PIpline 按顺序应用变换列表和最终估算器。
- 第15课：[评估指标](./evaluation)，如何知道我们的分类器是否表现良好？分类器的不同评估指标。
- 第16课：[最终项目](./final_project)，在此项目中，将扮演侦探，运用机器学习技能构建一个算法，通过公开的安然财务和邮件数据集，找出有欺诈嫌疑的安然雇员。

## 项目准备

1. 检查你是否装有可用的 Python，版本最好是 3.7，课程原来 Github 项目使用 Python 版本为 2.7，本项目所有代码均将使用 3.7 版本替换，Scikit-learn 版本 0.21.
2. 我们会使用 pip 来安装一些包。首先，从[此处](https://pip.pypa.io/en/latest/installing.html)获取并安装 pip。
3. 使用 pip 安装一系列 Python 包：
   - 转到终端行界面（请勿打开 Python，只打开命令提示符）
   - 安装 Scikit-learn: **pip install scikit-learn**
   - [此处](http://scikit-learn.org/stable/install.html)包含 Scikit-learn安装说明，可供参考
4. 安装自然语言工具包：**pip install nltk**

你只需操作一次，基础代码包含所有迷你项目的初始代码。进入 **tools/** 目录，运行 **startup.py**。该程序首先检查 python 模块，然后下载并解压缩我们在后期将大量使用的大型数据集：**安然数据集**。下载和解压缩需要一些时间，但是你无需等到全部完成再开始第一部分。

## 安然数据集

安然欺诈案是一个混乱而又引人入胜的大事件，从中可以发现几乎所有想像得到的企业违法行为。安然的电子邮件和财务数据集还是巨大、混乱的信息宝藏，而且，在你稍微熟悉这些宝藏后，它们会变得更加有用。我们已将这些电子邮件和财务数据合并为一个数据集，而你将在此迷你项目中研究它。

POI (Person Of Interest) 指的是在这个问题中的相关人物。

建议你在有时间的时候，花一个半小时，看一下【纪录片】安然：房间里最聪明的人 Enron: The Smartest Guys in the Room ( [Youtube链接](https://www.youtube.com/watch?v=rDyMz1V-GSg) )来了解这个事件。

**下载数据集**

目前从[CMU 安然数据集页面](https://www.cs.cmu.edu/~./enron/) 能下载到的最新数据集为 **[May 7, 2015 Version of dataset](https://www.cs.cmu.edu/~./enron/enron_mail_20150507.tar.gz)**.

## 介绍一个完整的机器学习项目流程

> imhuay/Algorithm_Interview_Notes-Chinese/[A-机器学习](https://github.com/imhuay/Algorithm_Interview_Notes-Chinese/tree/master/A-%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0)

1. 数学抽象

   明确问题是进行机器学习的第一步。机器学习的训练过程通常都是一件非常耗时的事情，胡乱尝试时间成本是非常高的。

   这里的抽象成数学问题，指的是根据数据明确任务目标，是分类、还是回归，或者是聚类。

2. 数据获取

   数据决定了机器学习结果的上限，而算法只是尽可能逼近这个上限。

   数据要有代表性，否则必然会过拟合。

   对于分类问题，数据偏斜不能过于严重（平衡），不同类别的数据数量不要有数个数量级的差距。

   对数据的量级要有一个评估，多少个样本，多少个特征，据此估算出内存需求。如果放不下就得考虑改进算法或者使用一些降维技巧，或者采用分布式计算。

3. 预处理与特征选择

   良好的数据要能够提取出良好的特征才能真正发挥效力。

   预处理/数据清洗是很关键的步骤，往往能够使得算法的效果和性能得到显著提高。归一化、离散化、因子化、缺失值处理、去除共线性等，数据挖掘过程中很多时间就花在它们上面。这些工作简单可复制，收益稳定可预期，是机器学习的基础必备步骤。

   筛选出显著特征、摒弃非显著特征，需要机器学习工程师反复理解业务。这对很多结果有决定性的影响。特征选择好了，非常简单的算法也能得出良好、稳定的结果。这需要运用特征有效性分析的相关技术，如相关系数、卡方检验、平均互信息、条件熵、后验概率、逻辑回归权重等方法。

4. 模型训练与调优

   直到这一步才用到我们上面说的算法进行训练。

   现在很多算法都能够封装成黑盒使用。但是真正考验水平的是调整这些算法的（超）参数，使得结果变得更加优良。这需要我们对算法的原理有深入的理解。理解越深入，就越能发现问题的症结，提出良好的调优方案。

5. 模型诊断

   如何确定模型调优的方向与思路呢？这就需要对模型进行诊断的技术。

   过拟合、欠拟合 判断是模型诊断中至关重要的一步。常见的方法如交叉验证，绘制学习曲线等。过拟合的基本调优思路是增加数据量，降低模型复杂度。欠拟合的基本调优思路是提高特征数量和质量，增加模型复杂度。

   误差分析也是机器学习至关重要的步骤。通过观察误差样本，全面分析误差产生误差的原因:是参数的问题还是算法选择的问题，是特征的问题还是数据本身的问题......

   诊断后的模型需要进行调优，调优后的新模型需要重新进行诊断，这是一个反复迭代不断逼近的过程，需要不断地尝试， 进而达到最优状态。

6. 模型融合/集成

   一般来说，模型融合后都能使得效果有一定提升。而且效果很好。

   工程上，主要提升算法准确度的方法是分别在模型的前端（特征清洗和预处理，不同的采样模式）与后端（模型融合）上下功夫。因为他们比较标准可复制，效果比较稳定。而直接调参的工作不会很多，毕竟大量数据训练起来太慢了，而且效果难以保证。

7. 上线运行

   这一部分内容主要跟工程实现的相关性更大。工程上是结果导向，模型在线上运行的效果直接决定模型的成败。不单纯包括其准确程度、误差等情况，还包括其运行的速度(时间复杂度)、资源消耗程度（空间复杂度）、稳定性是否可接受。

   这些工作流程主要是工程实践上总结出的一些经验。并不是每个项目都包含完整的一个流程。这里的部分只是一个指导性的说明，只有多实践，多积累项目经验，才会有自己更深刻的认识。

## 错误

[错误记录](./tools/errors_solution.md)


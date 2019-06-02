<br>
# Thesis-for-Graduation

This is the graduation thesis for a bachelor in Wuhan University. This project is mainly about the Boosting method. I compared and deduced
Adaboost, GBM and XGboost theoretically and implemented the simulation to compare the experimental results.

## Main work

本文基于boosting的几种算法，深入分析了其提出的理论背景与思路历程，比 较这几种算法理论背景与实际表现的异同。由Boosting的理论特性与提出动机，将 boosting 归纳为一种非参学习方法。

从统计的角度出发，得出 Adaboost 的实质是 一种stagewiseforward可加模型，其使用了指数损失来调优，具体的表现为调节样本权重。从可加模型的角度出发，将GBM是一种非参中的函数估计，也即在函数 空间上的一种优化。其计算核心为最速下降法，但与传统的梯度优化不同，其并没有将每一步的梯度作为方向，而是用弱分类器（决策树）去拟合每一步的梯度，后根据可加模型的思想，将弱分类器加入到现在的估计函数中进行优化。

XGBoost 在 GBM 的基础上进一步拓展。其计算核心为牛顿方法，所以 XGBoost 的优化有 时也被称为 NewtonBoosting。XGBoost 用二次梯度来决定优化方向，使用二阶泰 勒展开来拟合当前目标损失函数。运用这一思想，可以重新定义一种构建树的算 法（与基尼系数，信息熵类似），此算法决定了决策树中怎样选择节点可以达到最 大的准确率。

在实际数据算法比较中，与我们的理论结果相符，GBM与XGBoost 有着最好的预测准确率，也是现在被广泛使用的原因。本文还有一些未解决问题， 如 XGBoost 有着更好的收敛率，但实际操作中训练的时间较久，这种弊端是否可 以避免，是否与其估计贪婪算法的运用有关。这些问题在之后需要做进一步的探 究。

## Data
[**MNIST**](http://yann.lecun.com/exdb/mnist/)

## Reference
Mainly the references in the paper.


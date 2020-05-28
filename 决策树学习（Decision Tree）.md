

# 决策树学习（Decision Tree）

决策树学习是一种常见的数据挖掘方法，目的是根据一些已知数据建模来预测数据。

参考文档：

[Decision_tree_learning.pdf](../CSC1001/Assignments/Group/References/Decision_tree_learning.pdf) 

[CART.pdf](../CSC1001/Assignments/Group/References/CART.pdf) 

[section-11.pdf](../CSC1001/Assignments/Group/References/section-11.pdf) 

[HT17_lecture13.pdf](../CSC1001/Assignments/Group/References/HT17_lecture13.pdf) 

## Classification 决策树

![Screen Shot 2020-05-09 at 8.30.44 PM](/Users/yanghaowen/Documents/Notes/References/Images/classifucation_tree_illustration.png)

最常用的例子如上，要通过一系列限制条件来决定最终的点是圈圈还是叉。通过某种方式生成的决策树将长成这样：

![Screen Shot 2020-05-09 at 8.34.01 PM](/Users/yanghaowen/Documents/Notes/References/Images/classifucation_tree_illustration2.png)

## 如何训练 Classification 决策树

延续以上有两个特征（x和y）的模型，我们的数据集将可以写作：

$D = \{ ( x_ i , y_ i ) \} ^N _{i=1}$

这里 $x_i \in X$ 以及 $y_i \in Y$ ,暂且不考虑 $X$ , 而 $Y = \{ 1,...,K \}$ 是 $K$ 个分类标签。

定义以下符号：

总的数据的点的数量：$N$

特征 $y$ 的值为 $j \in Y$ 的点的数量：$N_j$



考虑这样一个节点：已经根据 $x$ 进行了一次划分, 所有的点的 $x$ 值都是 $X$ 的一个子集，我们称之为 $t$ 节点。

定义以下符号：

$t$ 节点中所有样本点的集合：$D(t)$

$t$ 节点中所有样本点的总数：$N(t)$

$t$ 节点中 $y$ 值为 $j \in Y$ 的样本点的数量：$N_j(t)$



现在一个人随机从 $D$ 中抽取样本，假设抽取 $j \in Y$ 标签的概率为 $\pi (j) = \frac{N_j}{N}$

那么抽取到在 $t$ 节点中且标签为 $j$ 的样本点的概率是：

$p(j,t) = \frac{N_j(t)}{N} =\frac{\pi(j)N_j(t)}{N_j}$

而抽取到了在 $t$ 节点的样本点的概率是：

$p(t) = \frac{N(t)}{N} = \displaystyle\sum_j{p(j,t)}$

而在 $t$ 节点中能抽到标签为 $j$ 的样本点的概率是：

$p(j|t) = \frac{N_j(t)}{N(t)}= \frac{p(j, t)}{p(t)}$

### 不纯度与节点的分裂：

定义：不纯度函数（Inpurity Function） $\phi (p_1,p_2, ... p_K)$ , 其中 $p_i > 0$ 且全部的和为1.

$\phi (p_1,p_2, ... p_K) \geq 0$

$\phi (\frac{1}{K},\frac{1}{K}, ... \frac{1}{K})$ 取到最大值

关于 $p_1,p_2, ... p_K$ 对称

$p_1,p_2, ... p_K$ 任何一个值为1，此时其余值为0，函数值为 0

#### 熵不纯度(Entropy impurity)：

$\phi (p_1,p_2, ... p_K) = -\displaystyle\sum_i{p_i \log{p_i}}$

#### 基尼不纯度(Gini impurity)：

$\phi (p_1,p_2, ... p_K) = \frac{1}{2}\displaystyle\sum_i{p_i(1-p_i)} = \displaystyle\sum_{i < j}{p_i p_j}$

那么

#### 节点的不纯度：

$i(t) = \phi(p(1|t),··· ,p(K|t))$



所以，通常的二元分裂原则是选择最能降低节点不纯度的分裂方式。



<img src="/Users/yanghaowen/Documents/Notes/References/Images/classifucation_tree_splitting_illustration.png" alt="Screen Shot 2020-05-09 at 9.27.50 PM" style="zoom:50%;" />

假设某个节点从 $t$ 分裂为 $t_L$ 和 $t_R$ ,

定义 $p_L = p(t_L)/p(t)$ 以及 $ p_R = p(t_R)/p(t) $ ，因此 $p_L + p_R = 1$



#### 不纯度减小量：

记对 $t$ 的某种分裂方式为 $S$

$\Delta i (S,t) = i(t) - p_L i(t_L) - p_R i(t_R)$



#### 节点在决策树中的不纯度

$I(t) = i(t)p(t)$



#### 则某种分裂对于决策树的不纯度减小量为：

$\Delta I (S,t) = I(t) - p_L I(t_L) - p_R I(t_R)$

而且可以推导出以下性质：

$\Delta I (S,t) = \Delta i (S,t) p(t)$



#### 决策树的不纯度

记决策树全部末端节点为集合 $\tilde T$

$I(T) = \displaystyle\sum _{t \in \tilde T} I(t) = \displaystyle\sum _{t \in \tilde T} i(t)p(t)$



所以如何决定分类标准 $j^*$ ?

还需要一些定义：



### 连续值处理：

https://blog.csdn.net/u012328159/article/details/79396893
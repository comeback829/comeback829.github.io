---
title: 动手学深度学习09
date: 2023-06-29 +0800
categories: [Machine Learning]
tags: [studynotes]   
math: true

---
## 课堂内容

1. softmax函数是确定的，softmax完以后进行最大似然估计，即最小化负对数似然，得到的结果是交叉熵,这个交叉熵即为损失函数

2. [softmax导数推导](https://zh.d2l.ai/chapter_linear-networks/softmax-regression.html)

   损失函数的导数是我们softmax模型分配的概率与实际发生的情况（由独热标签向量表示）的差

3. 损失函数

  ​	a. L2 loss
$$
  l(y,y\prime)=\frac{1}{2}{(y-y\prime)}^2
$$
  ​		离原点远时，逼近步幅太大

  ​	 b. L1 loss
$$
l(y,y\prime)=|y-y\prime|
$$
  ​		步幅稳定但原点处不可导且突变

  ​	 c. Huber's Robust Loss
$$
l(y,y\prime)=\begin{cases}
  l(y,y\prime)=\frac{1}{2}{(y-y\prime)}^2& if|y-y\prime|>1\\
  l(y,y\prime)=|y-y\prime|&otherwise
  \end{cases}
$$

4. 图像分类数据集

   ```python
   mnist_train =torchvision.datasets.FashionMNIST(root="../data",train=True(表示训练数据集), transform=trans,出来是以张量形式读取 download=True)
   ```

5. 从零实现softmax

​		a. 对矩阵进行softmax操作

​			为什么是矩阵：因为是批量操作，本来1维度，多了batch_size的第二维度

​		b. [高级索引](https://www.runoob.com/numpy/numpy-advanced-indexing.html)

​		c. 一行代码实现交叉熵
​			y是一个一维数组, $y_i$ 的值表示第i个样本中正确的分类是第几项

```python 
-torch.log(y_hat[range(len(y_hat)), y])
```


## 作业
---
title: 动手学深度学习08
date: 2023-07-04 +0800
categories: [Machine Learning]
tags: [studynotes]   
math: true
---
## 课堂内容

### 规范化流程 

1. ```python
   data_iter(batch_size, features, labels)##数据迭代器，专门用来批量取数据
   ```

2. ```python
   net(X)##模型
   ```

3. ```python
   loss(y_hat,y)##y_hat预测值，y正确值
   ```

4. ```python
   updater(params,lr,batch_size)##优化函数,如sgd梯度下降
   ```

5. 所有所需定义完毕后，训练(优化方法为梯度下降法)

   ```python
   epochs##训练轮次
   for epoch in range(epochs)
   	l=loss()
   	l.sum().backward()
       updater()
   ```

   



## 作业 


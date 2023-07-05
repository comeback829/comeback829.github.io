---
title: 动手学深度学习10
date: 2023-07-04 +0800
categories: [Machine Learning]
tags: [studynotes]   
math: true
img_cdn: https://cdn.jsdelivr.net
---

## 课堂内容

1. ![数学推导](/gh/comeback829/picture/blognote/math.jpg)

2. 感知机是二分类模型，不能分类XOR问题

3. 必定是非线性激活函数，否则多层后仍然是线性，不能解决问题

4. 矩阵乘法

   1. 点乘

      *，`torch.mul()`

   2. 叉乘

      `torch.matmul(A,B)`(有广播机制)，`torch.mm(A,B)`(无广播机制),A@B


 5. 训练设置多层感知机的超参数

    假设输入128 输出2

    先试128-->2,再试128-->16-->2,然后128-->32-->2,后面再加第三层，etc

## 作业


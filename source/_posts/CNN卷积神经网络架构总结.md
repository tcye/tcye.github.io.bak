---
title: CNN卷积神经网络架构总结
date: 2017-09-29 13:30:35
tags: 机器学习
categories: 机器学习
---

**注：本文将会以论文读后笔记的形式呈现，后续不断补充占坑**

## An Analysis Of Deep Neural Network Models For Practical Applications

在此综述下总结下2015年前的主流CNN架构及其贡献

1. LeNet5(1998):
    * CNN三特性: 局部感知、下采样、权值共享
    * 采用三层架构：卷积、下采样、非线性激活函数(tanh, sigmoid)，多层神经网络(MLP)作为最后的分类器
    * 后续的CNN架构大多基于LeNet5的这些特性，然而由于当时硬件计算能力限制，后续很长时间神经网络没有发展
2. AlexNet(2012): 赢的2012ImageNet冠军，从LeNet5的5层增加到7层
    * 使用ReLU作为激活函数，降低计算量
    * 引入Dropout防止过拟合
    * 引入Max-Pooling技术
    * 使用双GPU，分group卷积，显著减少训练时间
<!-- more -->
3. Network In Network(2013):
    * 首次提出在卷积层后再紧跟一个1x1的卷积核对特征进行融合，有效合并卷积特征，减少网络参数
    * 违背了LeNet在浅层使用大卷积核的设计原则，但取得了良好效果
4. VGG(2014):
    * 相比AlexNet使用9x9,11x11这样的大卷积核，VGG使用连续的3x3卷积核，可以获得同样的感受野，而参数数量和计算量可以显著减少
5. GoogleNet(2014):
    * 提出了Inception局部网络，并通过堆积Inception这样的局部小网络组成大网络
    * 类似NiN，使用了1x1的卷积核大幅减少参数数量和计算，即现在的流行的bottlenect layer
    * Bottlenect Layer: 先使用1x1卷积减少特征channel数量，再进行卷积，最后再用1x1卷积恢复特征数量，成功的原因是输入特征是相关的，可以适当的用1x1卷积去除冗余
6. Inception V3(2015):
    * 提出Batch-Normalization，对层的输入进行归一化，有助于训练

最后，使用论文中的一张神图结束这篇论文的笔记，准确率-时间复杂度-参数数量都在下图中很好的呈现了。
![acc-ops](/images/acc_vs_net_vs_ops.png)

2015年前的架构及贡献大致如此，目前更多的都是基于ResNet思想的架构，采用Identity-Map的结构，利于训练超深卷积神经网络

## ResNet

## Wide ResNet

## ResNeXt

## DenseNet

## Dual Path Networks (DPNs)

## Squeeze-and-Excitation Networks (SENet)

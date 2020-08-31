## 定义
分裂-变换-融合

## 相关论文
split-transform-merge strategy

resent，inception 以及它们的变体

### 2017
- **ResNeXt**: Aggregated Residual Transformations for Deep Neural Networks

### 2020

**VCRNet**: Visual Concept Reasoning Networks
与 resnext 一样采取 split-transform-merge strategy，但是
> While it explicitly has multiple branches to simultaneously learn
multiple visual concepts or properties, it only considers the dependencies or interactions between
them by using dense and local operations. We extend the architecture by split-transform-attendinteract-
modulate-merge stages, and this allows to capture the global context by reasoning with
sparse interactions between high-level visual concepts from different branches.

这篇论文可以在高级视觉概念间实现推理，之前的论文用的是local的信息进行交互，没有

## 参考
2017 [An Overview of ResNet and its Variants](https://towardsdatascience.com/an-overview-of-resnet-and-its-variants-5281e2f56035)
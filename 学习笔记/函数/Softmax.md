## 公式

$$ Softmax(x_i)=\frac{\exp(x_i)}{\sum_j\exp(x_j)} $$

### CrossEntropy Loss in Pytorch
This criterion combines nn.LogSoftmax() and nn.NLLLoss() in one single class[1]().
Pytorch官方文档里给出，交叉熵就是softmax和NLL loss的结合


### 参考

[CROSSENTROPYLOSS](https://pytorch.org/docs/master/generated/torch.nn.CrossEntropyLoss.html)
[Pytorch里的CrossEntropyLoss详解](https://www.cnblogs.com/marsggbo/p/10401215.html)


# SENet

## insight

> In SENet, Channel-Wise Attention enables the model to learn the weight of each channel, and then multiplies the weight back to the original channel. The features of those important channels are enhanced, and the insignificant are weakened, so that the extracted features are more directional and the network predicts better.
[Channel Distillation: Channel-Wise Attention for Knowledge Distillation](https://arxiv.org/abs/2006.01683)

SENet 具有 channel-wise attention


# Channel Distillation

>We use GAP to calculate the importance of each channel’s feature map, which represnets attention information of each channel. Then we consider the attention information of each channel’s feature map as knowledge. The

仅用了 GAP 去计算特征图的weights

## bug
![](../../.local/se_bug.png)


#



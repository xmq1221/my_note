## GPU、CPU 自动加载
```python
import torch

device = 'cuda' if torch.cuda.is_available() else 'cpu'
x = x.to(device)
```

## 判断 tensor 的设备
```python
x = torch.randn(3, 4, 5, device='cuda:0')
>>> x.get_device()
0
>>> x.cpu().get_device()  # RuntimeError: get_device is not implemented for type torch.FloatTensor
```
> get_device() -> Device ordinal (Integer) 
For CUDA tensors, this function returns the device ordinal of the GPU on which the tensor resides. For CPU tensors, an error is thrown.

在 cuda 上会返回卡号， cpu上会报错

#### 参考
[torch.Tensor.get_device](https://pytorch.org/docs/1.5.0/tensors.html?highlight=get_device#torch.Tensor.get_device)


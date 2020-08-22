## GPU、CPU 自动加载
```python
import torch

device = 'cuda' if torch.cuda.is_available() else 'cpu'
x = x.to(device)
```

## 判断 tensor 的设备
```python
>>> x = torch.randn(3, 4, 5, device='cuda:0')
>>> x.get_device()
0
>>> x.cpu().get_device()  # RuntimeError: get_device is not implemented for type torch.FloatTensor
```

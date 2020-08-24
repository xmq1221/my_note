# 输出较长的字符串
## 原长度
太长了，很丑也不方便看
```language
"/home/xx/new_projectX/code/image-classification-pytorch/"snapshot/flat/cifar10/resnet18/flat-191.pkl"
```

## 方法1
使用括号括起来
```language
("/home/xx/new_projectX/code/image-classification-pytorch/"
"snapshot/flat/cifar10/resnet18/flat-191.pkl")
```

# 字典
## json
```python
>>> import json
>>> json.dumps(mapping, indent=4, sort_keys=True)

{
    "a": 23,
    "b": 42,
    "c": 12648430
}

```

## Anaconda

### 换源
打开
```language
vi .condarc
```

输入清华镜像中列出的


#### 参考
[Anaconda 镜像使用帮助](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)


## pip

### 换源
打开
```language
vi ~/.pip/pip.conf
```

添加清华源
```language
[global]
index-url = https://mirrors.tuna.tsinghua.edu.cn/pypi/web/simple/
trusted-host = mirrors.tuna.tsinghua.edu.cn
```


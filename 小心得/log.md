## tee 与 >

### >
仅输出到日志文件中，屏幕不显示输出
```language
python train.py > log.txt
```

### tee
输出到屏幕和日志文件中, 2>&1 指将错误的输出结果也输出到日志文件
```language
python train.py 2>&1 | tee log.txt
```
#### 带有时间的log文件名
TO-DO

## 使用python中的log

~~TO-DO~~ 已做完

```python
import logging
```


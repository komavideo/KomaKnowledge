Tensorflow - 测试你的环境是否支持GPU运算
====================================

## 视频链接

https://youtu.be/LRN6XpEwKXg

## 知识点

* tensorflow的config包的使用

## API参考

https://www.tensorflow.org/

## 实战演习

```python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '3'
import tensorflow as tf

os.system("clear")

print("GPU列表：", tf.config.list_physical_devices('GPU'))
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

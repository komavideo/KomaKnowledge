Counter - 自动计算元素个数
========================

## 视频链接

https://youtu.be/WTZzYLLdTTc

## 知识点

* 计算数组元素个数的几个方法

## 实战演习

```python
# 定义有重复数据的数组
mylist = ['a', 'a', 'a', 'a', 'b', 'c', 'c']
# 使用len函数
print(len(mylist))
# 使用数组的count函数
print(mylist.count('a'))
print(mylist.count('b'))
print(mylist.count('c'))
print(mylist.count('d'))
# Counter登场
from collections import Counter
result = Counter(mylist)
print(result)
print('a:', result['a'])
# Counter的枚举属性
print(result.keys())
print(result.values())
print(result.items())
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

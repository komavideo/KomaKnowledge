deque - 双向队列的使用方式
========================

## 视频链接

https://youtu.be/t7jwPDkhCAo

## 知识点

* 使用Python集合包中的deque双向队列

## 实战演习

```python
# 双向队列
from collections import deque

# 声明队列
d = deque()
print(d)

# 初始化一个数组
d = deque(['a', 'b', 'c'])
print(d)

# 从右侧加入一个元素
d.append(1)
print(d)

# 从左侧加入一个元素
d.appendleft(10)
print(d)

# 从右侧加入一个数组
d.extend([2,3])
print(d)

# 从左侧加入一个数组
d.extendleft([20,30])
print(d)

# 在索引3之前插入100
d.insert(3, 100)
print(d)

# 右边弹出元素
a = d.pop()
print(a)
print(d)

# 左边弹出元素
a = d.popleft()
print(a)
print(d)

# 清除所有元素
d.clear()
print(d)

# 最大长度限制
d = deque([], maxlen=4)
for i in range(10):
    d.append(i)
    print(d)
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

[Python3]zip - 压缩你的数组，大家挤一挤吧
=====================================

## 视频链接

https://youtu.be/kdJCgoyvceU

## 知识点

* 使用zip函数将多个数组打包输出

## 实战演习

```python
def run():
    names = ["curry", "lebron", "durant"]
    ages = [32, 35, 31]

    # 循环数组输出
    for i in range(len(names)):
        print(names[i], "is", ages[i])

    # 压缩两个数组
    for name, age in zip(names, ages):
        print(name, "is", age)

    # 压缩三个数组
    points = [28, 21, 30]
    for name, age, point in zip(names, ages, points):
        print(name, "is", age, "got", point)

run()
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

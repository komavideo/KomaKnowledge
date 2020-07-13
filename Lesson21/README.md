【Tensorflow】矩阵计算评测 - CPU GPU 到底哪个快？
============================================

## 视频链接

https://youtu.be/chCe1EQ4f-s

## 知识点

* 分别使用CPU和GPU进行多矩阵计算

## 实战演习

```python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '3'
import timeit
import tensorflow as tf

def run():
    n = 1000
    # CPU计算矩阵
    with tf.device('/cpu:0'):
        cpu_a = tf.random.normal([n, n])
        cpu_b = tf.random.normal([n, n])
        print(cpu_a.device, cpu_b.device)
    # GPU计算矩阵
    with tf.device('/gpu:0'):
        gpu_a = tf.random.normal([n, n])
        gpu_b = tf.random.normal([n, n])
        print(gpu_a.device, gpu_b.device)

    def cpu_run():
        with tf.device('/cpu:0'):
            c = tf.matmul(cpu_a, cpu_b)
        return c 

    def gpu_run():
        with tf.device('/gpu:0'):
            c = tf.matmul(gpu_a, gpu_b)
        return c

    number = 1000

    print("初次运行：")
    cpu_time = timeit.timeit(cpu_run, number=number)
    gpu_time = timeit.timeit(gpu_run, number=number)
    print("", "CPU计算时间：", cpu_time)
    print("", "GPU计算时间：", gpu_time)

    print("再次运行：")
    cpu_time = timeit.timeit(cpu_run, number=number)
    gpu_time = timeit.timeit(gpu_run, number=number)
    print("", "CPU计算时间：", cpu_time)
    print("", "GPU计算时间：", gpu_time)

run()
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

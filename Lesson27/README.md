【Python】Trio - 一个友好的Python异步多线程框架，提升系统速度哦
========================================================

## 视频链接

https://youtu.be/knfwCVO9Llk

## 知识点

* Python多线程开发框架Trio的使用方法

## 官网

https://trio.readthedocs.io/

## 安装

```bash
$ pip install -U trio
```

## 实战演习

```python
import trio
import numpy as np

async def main():
    async with trio.open_nursery() as nursery:
        # 创建一个通道
        send_channel, receive_channel = trio.open_memory_channel(0)
        # 执行线程，传入通道对象
        nursery.start_soon(thread1, send_channel)
        nursery.start_soon(thread2, receive_channel)

async def thread1(send_channel):
    print("我是线程1，我是公司老板。")
    async with send_channel:
        for i in range(10):
            # 休息一会
            await trio.sleep(1.)
            # 给秘书发指示
            cmd = np.random.randint(10)
            print(">老板发出指示：{!r}".format(cmd))
            await send_channel.send(cmd)

async def thread2(receive_channel):
    print("我是线程2，我是个小秘书。")
    async with receive_channel:
        # 等待老板的指示
        async for value in receive_channel:
            print("+秘书收到指示：{!r}".format(value))

trio.run(main)
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

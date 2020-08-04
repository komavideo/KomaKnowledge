FastAPI - 快速的Web框架，不输Go与Node.js
======================================

## 视频链接

https://youtu.be/zZhLdylyABc

## 知识点

* FastAPI的基本使用

## 官网

https://fastapi.tiangolo.com/

## 特点

+ 运行快速，堪比Go与Node
+ 开发快速
+ 不易产生Bug
+ 很好的编辑器支持，直感开发
+ 简单，易学易用
+ 短小，代码量少
+ 健壮，适合产品级应用
+ 标准，符合OpenAPI和JSON规范

## 实战演习

```bash
# 安装
$ pip install fastapi
# ASGI安装(WSGI的升级版，支持异步调用)
$ pip install uvicorn
```

## main.py

```python
from typing import Optional
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "World"}

@app.get("/items/{item_id}")
def read_item(item_id: int, q: Optional[str] = None):
    return {"item_id": item_id, "q": q}
```

## 运行

```bash
$ uvicorn main:app --reload --port 8000
$ curl http://127.0.0.1:8000
$ curl http://127.0.0.1:8000/items/1
```

## API接口调试(Swagger UI)

```
http://127.0.0.1:8000/docs
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

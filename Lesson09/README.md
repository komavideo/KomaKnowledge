【Python】googletrans - 活用Google翻译API，拓展你的知识范围
======================================================

## 视频链接

https://youtu.be/ZQ77IXlZ0j0

## 知识点

+ Google翻译API(googletrans)的基本使用

## 官网

https://pypi.org/project/googletrans/

## 特点

+ 快速可靠(它使用的是 translation.google.com 的服务器)
+ 自动语言检测
+ 批量翻译
+ 可定制的服务URL
+ 连接池
+ 支持HTTP2

## 安装

```bash
$ pip install googletrans
$ pip list
```

## 代码实战

```python
from googletrans import Translator

translator = Translator()

def detect(str):
    result = translator.detect(str)
    print(result)

detect('how are you')
detect('こんにちは')
detect('你好')

def translate(str, dest="zh-CN"):
    trans_result = translator.translate(str, dest)
    print(trans_result.text)

translate('how are you')
translate('こんにちは')
translate('你好')
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

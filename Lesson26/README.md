pytesseract - 分析提取图片文字, 支持中日英
======================================

## 视频链接

https://youtu.be/cWKFZnanqfU

## 知识点

* 使用Python库pytesseract实现图片文字提取

## 官网

https://github.com/madmaze/pytesseract

## 前提

需要安装 Tesseract OCR 软件包。

### Tesseract OCR - 提取图片中的文字内容，支持多语言

https://youtu.be/Csbp4EZ-1J8

## 实战演习

```bash
$ pip install Pillow
$ pip install pytesseract
```

## main.py

```python
from PIL import Image
import pytesseract

# 英语文字
print(pytesseract.image_to_string(Image.open("./01.png"), lang='eng'))

# 简体中文
print(pytesseract.image_to_string(Image.open("./02.png"), lang='chi_sim'))

# 日本语
print(pytesseract.image_to_string(Image.open("./03.png"), lang='jpn'))
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

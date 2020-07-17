Tesseract OCR - 提取图片中的文字内容，支持多语言
===========================================

## 视频链接

https://youtu.be/Csbp4EZ-1J8

## 知识点

* 在Ubuntu平台使用OCR文字扫描软件 - Tesseract OCR

## 官网

https://tesseract-ocr.github.io/

## 实战演习

```bash
$ sudo apt install tesseract-ocr
$ sudo apt install libtesseract-dev

# 在Ubuntu系统如果没有找到tesseract-ocr包的话，需要改写apt文件
$ sudo nano /etc/apt/sources.list
...
deb http://archive.ubuntu.com/ubuntu bionic universe
...
$ sudo apt update && sudo apt upgrade

# 安装确认
$ tesseract -v
# 确认支持的语言
$ tesseract --list-langs
# 安装新的语言包
# 简体中文
$ sudo apt install tesseract-ocr-chi-sim
# 日本语(vert:竖文字)
$ sudo apt install tesseract-ocr-jpn  tesseract-ocr-jpn-vert

# 使用测试
# 英文
$ tesseract 01.png out -l eng
# 简体中文
$ tesseract 02.png out -l chi_sim
# 日本语
$ tesseract 03.png out -l jpn
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

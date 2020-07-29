qrcode - 快速生成QR代码
======================

## 视频链接

https://youtu.be/dKlCCxZX7fU

## 知识点

* 使用Python快速生成QR代码

## 官网

https://github.com/lincolnloop/python-qrcode

## 安装

```bash
$ pip install qrcode
$ pip install pillow
# 命令行确认
$ qr "helo qrcode." > qrcode.png
```

## 实战演习

```python
import qrcode
from PIL import Image

qr = qrcode.QRCode(
    version=1, # 1-40
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=10,
    border=1,
)
qr.add_data('http://komavideo.com')
qr.make(fit=True)
img = qr.make_image(fill_color="black", back_color="white").convert('RGB')

# 个性化Logo
logo = Image.open('koma.png')
logo = logo.resize((80, 80), Image.LANCZOS)
pos = ((img.size[0] - logo.size[0]) // 2, (img.size[1] - logo.size[1]) // 2)
img.paste(logo, pos)

img.save('qrcode_test.png')
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

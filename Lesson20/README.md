OpenCV - 人脸检测模型，让我看看你是谁
=================================

## 视频链接

https://youtu.be/tkHyy3S6YC4

## 知识点

* OpenCV的人脸检测模型

## 实战演习

## 必要库安装

```bash
$ pip install opencv-python
```

## main.py

```python
import cv2

# 脸部模型
cascade_path = "./models/haarcascade_frontalface_default.xml"
# cascade_path = "./models/haarcascade_frontalface_alt.xml"
# cascade_path = "./models/haarcascade_frontalface_alt2.xml"
# cascade_path = "./models/haarcascade_frontalface_alt_tree.xml"

# 眼睛模型
# eye_cascade_path = 'models/haarcascade_eye.xml'
# eye_cascade_path = 'models/haarcascade_eye_tree_eyeglasses.xml'

def run(imgPath=""):
    outputPath = "./output.jpg"

    # 图片文件读取
    image = cv2.imread(imgPath)
    # 灰度化
    image_gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
    # 分类器取得
    cascade = cv2.CascadeClassifier(cascade_path)
    # 脸型检测
    facerect = cascade.detectMultiScale(image_gray, scaleFactor=1.1, minNeighbors=2, minSize=(30, 30))
    # 找到脸了
    if len(facerect) > 0:
        # 画出脸的位置
        for rect in facerect:
            cv2.rectangle(image, tuple(rect[0:2]),tuple(rect[0:2]+rect[2:4]), (0, 255, 0), thickness=3)

        # 眼睛检测
        # eye_cascade = cv2.CascadeClassifier(eye_cascade_path)
        # eyes = eye_cascade.detectMultiScale(image_gray)
        # for (ex, ey, ew, eh) in eyes:
        #     cv2.rectangle(image, (ex, ey), (ex + ew, ey + eh), (0, 255, 0), 2)

        # 结果保存
        cv2.imwrite(outputPath, image)
        print("找到脸了！")
    else:
        print("对不起，没有脸！")

run(imgPath="./face0.jpg")
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

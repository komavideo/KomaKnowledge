【Python3】venv - 自带的虚拟环境建立模块，不用virtualenv了
====================================================

## 知识点

* 使用Python自带的虚拟环境建立模块
* 使用最新的Python版本3.8.2
* 不再用virtualenv了，再见

### Virtualenv - Python虚拟环境, 三大神器之一

https://youtu.be/Y9JMfWAr_04

## 实战演习

```bash
###################################
# 在Linux中安装Python3.8
sudo apt install python3.8
# 安装Python3.8虚拟环境模块
sudo apt install python3.8-venv
# 建立虚拟环境
python3.8 -m venv myvenv

###################################
# 使用虚拟环境
cd myvenv
# 激活
source bin/activate
# 版本确认
python -V
pip -V
# 更新pip版本
python -m pip install --upgrade pip
python -m pip install --upgrade setuptools
pip list
# 安装numpy模块
pip install numpy
nano main.py
...
import numpy as np

myarray = np.array([1,2,3,4,5])
print(myarray)
...
python main.py
# 退出虚拟环境
deactivate
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

Miniconda - Python的包管理器，再见pip
==================================

## 视频链接

https://youtu.be/4EzO8I8kRtU

## 知识点

* 使用Conda工具管理Python虚拟环境和安装包

## 官网

https://docs.conda.io/en/latest/miniconda.html

## 实战演习

```bash
# Miniconda安装
$ MINICONDA_INSTALLER_SCRIPT=Miniconda3-latest-Linux-x86_64.sh
$ MINICONDA_PREFIX=/usr/local
$ wget https://repo.continuum.io/miniconda/$MINICONDA_INSTALLER_SCRIPT
$ chmod +x $MINICONDA_INSTALLER_SCRIPT
$ sudo ./$MINICONDA_INSTALLER_SCRIPT -b -f -p $MINICONDA_PREFIX
# 版本确认
$ conda --version
# 虚拟环境确认
$ conda info -e
# 已安装包确认
$ conda list
# 建立虚拟环境1
$ conda create -n _pml_ python=3.8
# 进入虚拟环境
$ source activate _pml_
# Python确认
$ python -V
$ which python
# 虚拟环境中安装包确认
$ conda list
$ conda install numpy
# 退出虚拟环境
$ conda deactivate
# 建立虚拟环境2
$ conda create -n _ptf_ python=3.7
$ source activate _ptf_
$ conda list
$ python -V
$ which python
$ conda search tensorflow
$ conda install tensorflow
$ conda deactivate
# 删除虚拟环境
$ conda remove -n _ptf_ --all
# conda本体更新
$ sudo conda update conda
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

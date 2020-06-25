【Linux】Linux下的包管理器-Linuxbrew (Homebrew)
============================================

## 视频链接

https://youtu.be/He_DvVlOdw8

## 知识点

+ macOS下的知名包管理器 Homebrew 在Linux环境下的安装与使用

## 官网

https://brew.sh/

### Linux安装向导

https://docs.brew.sh/Homebrew-on-Linux

## 安装

### 系统需要

+ 64-bit x86_64 CPU
+ Linux 2.6.32 or newer
+ GCC 4.7.0 or newer
+ Glibc 2.13 or newer

### 前期准备

+ *Debian* 或 *Ubuntu*

```bash
$ sudo apt-get install build-essential curl file git
```

+ *Fedora*, *CentOS*, 或 *Red Hat*

```bash
$ sudo yum groupinstall 'Development Tools'
$ sudo yum install curl file git
$ sudo yum install libxcrypt-compat # needed by Fedora 30 and up
```

### 开始安装

```bash
# 下面的命令会初始化系统用户 `linuxbrew` ，并以 `/home/linuxbrew/.linuxbrew` 为根目录，进行包的安装管理与使用。
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install.sh)"
# 更新用户使用环境配置文件
$ test -d ~/.linuxbrew && eval $(~/.linuxbrew/bin/brew shellenv)
$ test -d /home/linuxbrew/.linuxbrew && eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)
$ test -r ~/.bash_profile && echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile
# Debian/Ubuntu
$ echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.profile
# CentOS/Fedora/RedHat
$ echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile
# 安装确认
$ brew
$ which brew
```

## 使用

```bash
# 安装第一个包工具
$ brew install hello
$ hello
$ which hello

# 包更新
$ brew upgrade hello

# 静态网站生成工具
$ brew install hugo
```

### 可使用包一览

https://formulae.brew.sh/

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

Corretto - 基于OpenJDK的免费、多平台、生产用发行版
=============================================

## 视频链接

https://youtu.be/ejGNrStcBps

## 知识点

* Corretto，Amazon的OpenJDK版本

## 官网

https://aws.amazon.com/cn/corretto/

## 实战演习

```bash
# 注册Corretto信息库
$ wget -O- https://apt.corretto.aws/corretto.key | sudo apt-key add -
$ sudo add-apt-repository 'deb https://apt.corretto.aws stable main'
# 信息库更新
$ sudo apt -y update
$ sudo apt -y upgrade
# Corretto安装
$ apt search corretto
$ sudo apt install java-1.8.0-amazon-corretto-jdk
$ java -version
# Java代码测试
$ nano CMain.java
...
class CMain {
    public static void main(String args[]) {
        System.out.println("Helo Corretto.");
    }
}
...
$ javac CMain.java
$ java CMain
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

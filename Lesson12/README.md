在Ubuntu环境下搭建Ruby on Rails开发环境
====================================

## 视频链接

https://youtu.be/JMGHoAs26ag

## 知识点

* 在Linux下安装RVM
* 在Linux下安装Rails

## 实战演习

```bash
###############################################################################
# 前提：必要工具库安装
$ sudo apt install -y curl git gnupg2
###############################################################################
# 安装node.js
# https://github.com/nodesource/distributions/blob/master/README.md
$ curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
$ sudo apt update && sudo apt install -y nodejs
$ node -v
###############################################################################
# 安装yarn
# https://yarnpkg.com/lang/en/docs/install
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
$ sudo apt update && sudo apt install -y yarn
$ yarn -v
###############################################################################
# 安装rvm
# https://rvm.io/

$ gpg2 --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
$ \curl -sSL https://get.rvm.io | bash -s stable
$ echo "source $HOME/.rvm/scripts/rvm" >> ~/.bash_profile
# 将终端设为“以登录shell方式运行命令”
$ rvm -v
$ rvm list known
$ rvm install 2.6
$ rvm list
$ ruby -v
$ gem -v
$ rvm install 2.7
$ ruby -v
# 切换使用版本
$ rvm use ruby-2.6.5
$ ruby -v
# 设置默认使用版本
$ rvm --default use ruby-2.7.0
$ rvm list
$ #rvm alias create default 2.6
$ #rvm use 2.6
###############################################################################
# Ruby文件
$ nano main.rb
...
a = 3 ** 2
b = 4 ** 2
puts Math.sqrt(a+b)
...
$ ruby main.rb
###############################################################################
# 安装Rails6
$ gem install rails -v '6.0.3.2'
$ rails -v
$ rails new myweb
$ cd myweb
$ rails server --binding=192.168.1.1
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

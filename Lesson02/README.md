【网站开发】Hugo - 史上最快的建站工具
====================================

## 视频链接

https://youtu.be/07igyVZUUuA

## 知识点

+ 号称史上最快的建站工具 *Hugo* 的基本使用

## 官网

https://gohugo.io

## 安装

首先，请在 Linux 下安装 LinuxBrew 包管理工具。

```bash
$ brew install hugo
$ hugo help
$ hugo env
```

## 使用步骤

```bash
# 1.建立以个网站
$ hugo new site myweb
$ cd myweb
$ nano config.toml
...
baseURL = "http://xxx.example.org/"
languageCode = "zh"
title = "小马技术站"
...
# 其他可以设置的内容
$ hugo config
# 2.加入一个主题(https://themes.gohugo.io/)
# https://themes.gohugo.io/hyde-hyde/
$ mkdir themes
$ git clone https://github.com/htr3n/hyde-hyde.git themes/hyde-hyde
$ rm -rf themes/hyde-hyde/.git
$ cp themes/hyde-hyde/exampleSite/config.toml ./

# 3.加入网站内容
#编辑页面默认生成模板
$ nano archetypes/default.md
...
This is my page.
中文测试。
日本語テスト。
...
$ hugo new posts/page1.md
$ hugo new posts/page2.md
$ hugo new posts/page3.md
# 99.建立静态网站
$ hugo
$ ls -l public/

# 使用hugo http服务
$ hugo server -D --bind 192.168.11.21 --baseURL http://192.168.11.21/
```

## 主要功能

+ 内容管理
  - 内容组织，语法高亮，内容格式，设置格式，短代码，内容章节，内容分类，内容布局，URL管理，菜单管理，静态文件，内容表TOC，图片处理，etc.
+ 模板
  - 查找顺序，定义输出，模板块，内容列表，主页模板，章节模板，分类模板，单页模板，内容显示模板，数据模板，局部模板，404页，菜单模板，分页管理，etc.
+ 函数
  - 牛毛
+ 变量
  - 牛毛
+ 管道
  - SASS/SCSS，PostCSS，资源最小化，资源打包，指纹识别，etc.
+ 插件
+ 部署

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

【Vue.js】Vue Cli 4.x - 越发完善的vue.js命令行工具
===============================================

## 视频链接

https://youtu.be/DKTWvqxuKyI

## 知识点

+ vue.js命令行工具最新版本的基本使用
+ Ubuntu 20.04 LTS/Node.js v12.x

## 官网

https://cli.vuejs.org/

## 安装使用

```bash
# 安装Node.js/npm
$ curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
$ sudo apt-get install -y nodejs
# 安装vue-clie
$ sudo npm install -g @vue/cli
# 版本确认
$ vue -V
# 命令行帮助
$ vue --help
# UI工具启动，并建立一个项目
$ vue ui
...
# UI工具的基本使用
# 安装依赖和插件，安装vuex, bootstrap等
...
# 调整开发服务器端口(配置参考:https://cli.vuejs.org/zh/config/)
$ nano package.json
...
    "vue": {
        "devServer": {
            "port": 8088
        }
    },
...
# 启动调试工程
$ npm run serve
# 打包编译工程
$ npm run build
```

## 工程编辑

```bash
# 进入工程目录
$ cd myweb
# 启动编辑器
$ code .
```

### main.js

```js
import 'bootstrap/dist/css/bootstrap.css'
```

### HelloWorld.vue

在 HelloWorld.vue 组件中加入Bootstrap样式按钮

```html
<div>
    <button type="button" class="btn btn-primary">Primary</button>
    <button type="button" class="btn btn-secondary">Secondary</button>
    <button type="button" class="btn btn-success">Success</button>
    <button type="button" class="btn btn-danger">Danger</button>
    <button type="button" class="btn btn-warning">Warning</button>
    <button type="button" class="btn btn-info">Info</button>
    <button type="button" class="btn btn-light">Light</button>
    <button type="button" class="btn btn-dark">Dark</button>
    <button type="button" class="btn btn-link">Link</button>
</div>
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

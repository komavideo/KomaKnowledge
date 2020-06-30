Puppeteer - 使用 javascript(node.js) 抓取屏幕图像
===============================================

## 视频链接

https://youtu.be/4-X1CeFefp8

## 知识点

* 学习Google Puppeteer的基本抓图功能

## Puppeteer

Puppeteer是一个Node库，它提供了高级API来通过DevTools协议控制无头Chrome或Chromium。

### 官网

https://developers.google.com/web/tools/puppeteer

## 实战演习

```bash
# 建立一个node.js工程
$ mkdir myapp
$ cd myapp
$ npm init
# 安装puppeteer
$ npm install puppeteer --save
# 编辑网页抓屏代码
$ nano capit.js
```

```js
const puppeteer = require("puppeteer");

const run = async () => {
  const browser = await puppeteer.launch()
  const page = await browser.newPage()

  await page.setViewport({
    width: 640,
    height: 800
  })

  await page.goto('http://komavideo.com/')
  await page.screenshot({
      path: 'mypic.png',
      fullPage: true
  })

  await browser.close();
};

run();
```

```bash
# 执行网页抓取
$ node capit.js

Done.
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

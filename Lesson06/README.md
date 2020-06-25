【JavaScript】如何实现使用JavaScript画图呢？用HTML5画布(Canvas)呀
===============================================================

## 视频链接

https://youtu.be/7-EIqjYs6jY

## 知识点

+ 使用HTML5+JavaScript画个图看看

## 代码实战

### main.html

```html
<!DOCTYPE html>
<html lang="zh-cmn-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>JavaScript Art</title>
    <link rel="stylesheet" href="./main.css">
</head>
<body>
    <canvas id="mainCanvas" width="800" height="600"></canvas>    
    <script src="main.js"></script>
</body>
</html>
```

### main.css

```css
#mainCanvas {
    border: 3px solid gray;
}
```

### main.js

```javascript
// 获取画布对象，生成2d上下文
const canvas = document.querySelector("#mainCanvas")
const ctx = canvas.getContext("2d")

// ★★★注意：画布的坐标原点为左上角(0,0)

///////////////////////////////////////////////////////////
// 设置画笔填充样式
ctx.fillStyle = "gray"

// 画一个矩形：fillRect(x, y, w, h)
ctx.fillRect(50, 150, 100, 200)

///////////////////////////////////////////////////////////
// 设置描边样式
ctx.strokeStyle = "green"

// 画一个描边矩形(无填充)：strokeRect(x, y, w, h)
ctx.strokeRect(200, 150, 100, 200)

///////////////////////////////////////////////////////////
// 使用路径Path来画一个圆形
ctx.beginPath()

// 画圆：arc(x, y, radius, startAngle, endAngle)
ctx.arc(400, 150, 50, 0, Math.PI * 2)

// 填充样式
ctx.fillStyle = "gray"

// 描画填充
ctx.fill()

///////////////////////////////////////////////////////////
// 画一条弧线
ctx.beginPath()

// 画弧：arc(x, y, radius, startAngle, endAngle)
ctx.arc(400, 250, 50, 0, Math.PI)

// 填充样式
ctx.fillStyle = "pink"

// 描画填充
ctx.fill()

///////////////////////////////////////////////////////////
// 画出任意两点之间的连线
ctx.beginPath()

// 移动到起始点
ctx.moveTo(500, 250)

// 向目标点画一条线
ctx.lineTo(600, 350)

// 线的样式
ctx.strokeStyle = "blue"

// 描画
ctx.stroke()

```

## API参考(MDN)

https://developer.mozilla.org/zh-CN/docs/Web/API/Canvas_API/Tutorial

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

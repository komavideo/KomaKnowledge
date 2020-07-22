Bootstrap 5 - 小试牛刀
======================

## 视频链接

https://youtu.be/GnWgKwLPfjE

## 知识点

* Bootstrap 5 beta版的初体验

## 官网

https://v5.getbootstrap.com/

## 注目点

+ 取消jQuery依赖
+ 支持自己的JS插件
+ 停止IE支持
+ CSS自定制属性
+ Grid网格系统增强
+ Form组件增强
+ 提供丰富的图标库  
  https://icons.getbootstrap.com/
+ etc.

## 下载

### Bootstrap 5

https://v5.getbootstrap.com/docs/5.0/getting-started/download/

### Bootstrap Icons

https://icons.getbootstrap.com/

## 实战演习

```html
<!doctype html>
<html lang="zh">

<head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="/bootstrap-5.0.0-alpha1-dist/css/bootstrap.min.css">
    <title>Hello, world!</title>
    <style>
        .themed-grid-col {
            padding-top: .75rem;
            padding-bottom: .75rem;
            background-color: rgba(86, 61, 124, .15);
            border: 1px solid rgba(86, 61, 124, .2);
        }
        .themed-container {
            padding: .75rem;
            margin-bottom: 1.5rem;
            background-color: rgba(0, 123, 255, .15);
            border: 1px solid rgba(0, 123, 255, .2);
        }
    </style>
</head>
<body>
    <!-- Just an image -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">Navbar</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup"
                aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
                <div class="navbar-nav">
                    <a class="nav-link active" aria-current="page" href="#">Home</a>
                    <a class="nav-link" href="#">Features</a>
                    <a class="nav-link" href="#">Pricing</a>
                    <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
                </div>
            </div>
        </div>
    </nav>
    <div role="main">
        <div class="container">
            <h2>按钮展示</h2>
            <button type="button" class="btn btn-primary" onclick="alert('Bootstrap 5 is good.')">Primary</button>
            <button type="button" class="btn btn-secondary">Secondary</button>
            <button type="button" class="btn btn-success">Success</button>
            <button type="button" class="btn btn-danger">Danger</button>
            <button type="button" class="btn btn-warning">Warning</button>
            <button type="button" class="btn btn-info">Info</button>
            <button type="button" class="btn btn-light">Light</button>
            <button type="button" class="btn btn-dark">Dark</button>
            <button type="button" class="btn btn-link">Link</button>
        </div>
        <div class="container">
            <h2 class="mt-3">容器container响应布局</h2>
        </div>
        <div class="container themed-container">.container</div>
        <div class="container-sm themed-container">.container-sm</div>
        <div class="container-md themed-container">.container-md</div>
        <div class="container-lg themed-container">.container-lg</div>
        <div class="container-xl themed-container">.container-xl</div>
        <div class="container-xxl themed-container">.container-xxl</div>
        <div class="container-fluid themed-container">.container-fluid</div>
    </div>
    <div rold="body">
        <div class="container">
            <div class="row justify-content-start">
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
            </div>
            <div class="row justify-content-center">
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
            </div>
            <div class="row justify-content-end">
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
            </div>
            <div class="row justify-content-around">
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
            </div>
            <div class="row justify-content-between">
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
            </div>
            <div class="row justify-content-evenly">
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
                <div class="col-4 themed-grid-col">
                    One of two columns
                </div>
            </div>
        </div>
    </div>
    <div role="form" class="mb-5">
        <div class="container mb-5">
            <div class="mb-3">
                <label for="exampleFormControlInput1" class="form-label">Email address</label>
                <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com">
            </div>
            <div class="mb-3">
                <label for="exampleFormControlTextarea1" class="form-label">Example textarea</label>
                <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
            </div>
        </div>
    </div>
    <hr>
    <nav class="navbar fixed-bottom navbar-dark bg-dark mt-5">
        <div class="container">
            <div class="footer text-center">
                <a class="navbar-brand" href="#">@2020</a>
            </div>
        </div>
    </nav>
    <script src="/bootstrap-5.0.0-alpha1-dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

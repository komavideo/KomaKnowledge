Deno - 一个安全的Javascript和TypeScript运行时
==========================================

## 视频链接

https://youtu.be/RNx_fIYMNRs

## 知识点

* Deno的使用基础介绍
* Node.js的弟弟，生父Ryan Dahl(ライアン・ダール)

## 官网

https://deno.land/

## Deno vs Node

+ 不再使用npm（node_modules地狱）
+ 不再使用package.json
+ 所有的异步调用都返回Promise, 但与Node处理方式不同
+ 对于资源存取需要单独授权
+ 使用ES模块, 不支持require()
+ 第三方模块通过URL导入  
  ```import * as log from "https://deno.land/std/log/mod.ts";```

## Deno的特点

+ 沙盒机制，更安全的运行时(file, network, etc.)
+ 原生支持JavaScript和TypeScript
+ 异步处理采用Promise
+ 仅一个可执行的文件
+ 内置更多的实用程序
+ 有一套可信赖的标准库

## 实战演习

```bash
# 安装
$ curl -fsSL https://deno.land/x/install/install.sh | sh
# 安装确认
$ deno -V
$ deno --help
# 简单程序执行
$ deno run https://deno.land/std/examples/welcome.ts
```

## 建立一个http服务程序

```js
import { serve } from "https://deno.land/std@0.62.0/http/server.ts";
const s = serve({ port: 8000 });
console.log("http://localhost:8000/");
for await (const req of s) {
    req.respond({ body: "Hello World\n" });
}
```

### 运行

```bash
# Error
$ deno run main.ts
# 赋予权限运行
$ deno run --allow-net main.ts
```

## Servest - Deno Web开发框架

https://servestjs.org/

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

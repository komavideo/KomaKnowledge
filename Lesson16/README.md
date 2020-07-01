COVID-19 - 新冠来袭，看我捉到你
============================

## 视频链接

https://youtu.be/8RmvGDNsnwI

## 知识点

* 使用COVID-19获取新冠病毒最新数据
* 使用Rakuten Rapid API

## Rakuten RapidAPI

https://api.rakuten.net/

## COVID-19 API

https://api.rakuten.net/api-sports/api/covid-193/

## 实战演习

```
$ npm install unirest
```

### Statistics.js

取得全世界最新的感染数据。

```js
var unirest = require("unirest");
var req = unirest("GET", "https://covid-193.p.rapidapi.com/statistics");
req.headers({
	"x-rapidapi-host": "covid-193.p.rapidapi.com",
	"x-rapidapi-key": "key",
	"useQueryString": true
});
req.end(function (res) {
	if (res.error) throw new Error(res.error);
	console.log(JSON.stringify(res.body, null, 3));
});
```

### 获取中国数据, GetChina.js

```js
var unirest = require("unirest");
var req = unirest("GET", "https://covid-193.p.rapidapi.com/statistics");
req.query({
	"country": "China"
});
req.headers({
	"x-rapidapi-host": "covid-193.p.rapidapi.com",
	"x-rapidapi-key": "key",
	"useQueryString": true
});
req.end(function (res) {
	if (res.error) throw new Error(res.error);
	console.log(JSON.stringify(res.body, null, 3));
});
```

### 获取美国数据, GetUSA.js

```js
var unirest = require("unirest");
var req = unirest("GET", "https://covid-193.p.rapidapi.com/statistics");
req.query({
	"country": "USA"
});
req.headers({
	"x-rapidapi-host": "covid-193.p.rapidapi.com",
	"x-rapidapi-key": "key",
	"useQueryString": true
});
req.end(function (res) {
	if (res.error) throw new Error(res.error);
	console.log(JSON.stringify(res.body, null, 3));
});
```

### 获取所有国家代码, Countries.js

```js
var unirest = require("unirest");
var req = unirest("GET", "https://covid-193.p.rapidapi.com/countries");
req.headers({
	"x-rapidapi-host": "covid-193.p.rapidapi.com",
	"x-rapidapi-key": "key",
	"useQueryString": true
});
req.end(function (res) {
	if (res.error) throw new Error(res.error);
	console.log(JSON.stringify(res.body, null, 3));
});
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

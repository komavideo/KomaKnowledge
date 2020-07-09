JavaScript - 神奇的几个功能
=========================

## 视频链接

https://youtu.be/S80h0ZVYbIo

## 知识点

+ 函数构造器
+ 动态绑定属性
+ 【+】运算符做数值变换
+ 给函数分配属性
+ 函数的调用堆栈
+ 【void】无效操作符

## 实战演习

### 函数构造器

```js
const add = new Function("a", "b", "return a+b")
console.log(add(10,20))

const helo = new Function("name", "return 'helo '+name+'.'")
console.log(helo("koma"))
```

### 动态绑定属性

```js
const book = {
    title: 'I like javascript.',
    author: 'Mike',
    price: 50
}
with(book) {
    console.log("书名：", title)
    console.log("作者：", author)
    console.log("价格：", price)
}
```

### 【+】运算符做数值变换

```js
const age = +"25"
console.log("你的年龄是：", age+1)
```

### 给函数分配属性

```js
function helo(name) {
    if (helo.sex == "F") {
        console.log("你好，", name, "女士。")
    }else{
        console.log("你好，", name, ".")
    }
}
helo.sex = "F"
helo("Hatano")
```

### 函数的调用堆栈

```js
function func1() {
    console.log("func1():", arguments.callee.caller)
}
function func2() {
    func1()
}
func2()
```

### 【void】无效操作符

```js
console.log(void(1))
console.log(void(true))
console.log(void(false))
console.log(void({}))
console.log(void(undefined))

if (void(1)) {
    console.log("yes")
}else{
    console.log("no")
}
```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

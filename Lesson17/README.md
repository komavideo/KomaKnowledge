Marp for VS Code - 快速建立你的展示文档, 向powerpoint说再见
=======================================================

## 视频链接

https://youtu.be/uBmZEgGNnkk

## 知识点

* 在VS Code中安装Marp插件
* 通过Markdown语法建立ppt的展示类似文档
* 向powerpoint说再见吧

## Marp官网

https://marp.app/

### Marp for VS Code 插件

https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode

### 文档语法

https://marpit.marp.app/

## 实战演习

```markdown

---
marp: true
theme: uncover
size: 16:9
paginate: true
header: "Marp for VS Code 好用又方便"
footer: "by 小马视频"
---
Marp for VS Code
=================

快速建立你的展示文档, 向powerpoint说再见

---
<!--
_backgroundColor: black
_color: white
-->

# 知识点

* 在VS Code中安装Marp插件
* 通过Markdown语法建立ppt的展示类似文档
* 向powerpoint说再见吧

---

# Marp for VS Code 插件安装

https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode

---

# Python代码展示

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello():
    return '你好! 吃饭了吗？'

if __name__ == "__main__":
    app.run(host="0.0.0.0", debug=True, port=5000)
```

---
# Java代码展示

```java
import java.util.*;

class CMain 
{
    public static void main(String args[]) 
    {
        System.out.println("Helo Java.");
    }
}
```

---
<!--
color: white
-->

# FIFA 2020

![bg brightness:0.5](fifa2020.jpg)

---
# eFootball 2020

![bg brightness:0.5](efootball2020.jpg)

---
<!--
backgroundColor: purple
-->

# 我爱梅西

![bg left:80%](efootball2020.jpg)

---
# 我爱阿扎尔

![bg right:80%](fifa2020.jpg)

```

## 课程文件

https://github.com/komavideo

## 小马视频频道

http://komavideo.com

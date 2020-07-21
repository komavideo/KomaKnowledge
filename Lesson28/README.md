【Python】Beautiful Soup - 学英语了，走！爬单词去。
==============================================

## 视频链接

https://youtu.be/W-6J3ui-75I

## 知识点

* 使用Beautiful Soup爬取TOEIC单词表

## 官网

https://www.crummy.com/software/BeautifulSoup/

## 单词网站

http://www7b.biglobe.ne.jp/~browneye/english/

## 安装

```bash
$ pip install beautifulsoup4
```

## 实战演习

```python
import requests
from bs4 import BeautifulSoup

import time
import random

def run():
    page_url = "http://www7b.biglobe.ne.jp/~browneye/english/TOEIC400-1.htm"
    r = requests.get(page_url)
    r.encoding = r.apparent_encoding    

    soup = BeautifulSoup(r.text, features="html.parser")

    td_list = soup.find_all("td")
    td_values = [x.text for x in td_list]

    splited_list = []

    for index in range(0, len(td_values), 4):
        word_row = td_values[index: index + 4]

        if word_row[0] == '\u3000':
            continue
        splited_list.append(word_row)

    with open("toeic_words.txt", "w") as f:
        for value in splited_list:
            f.write("{},{}\n".format(value[1], value[2]))
        print("Yes, done.")

if __name__ == "__main__":
    run()
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

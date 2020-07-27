【Python】pytrends - 几个关键字，了解世界新动向
===========================================

## 知识点

* Google趋势的API pytrends 的使用方法

## 官网

https://github.com/GeneralMills/pytrends

## 实战演习

### 安装

```bash
$ pip install pytrends
```

### main.py

```python
from pytrends.request import TrendReq

pytrends = TrendReq(hl='ja-JP', tz=360)
trends = pytrends.trending_searches(pn='japan')
trends_values = trends.values.tolist()

google_trend_list = []
for value in trends_values:
    item = str(value[0])
    item = item.replace('　', '')
    item = item.replace(' ', '')
    google_trend_list.append(item)

print('google_trend_list = ' + str(google_trend_list))
```

### 自定义查询

```python
"""
查询期间指定：
timeframe='now 1-d' -> 过去1天
timeframe='today 1-m' -> 过去一个月
timeframe='today 5-y' -> 过去5年
"""
KEYWORD = '米中'
kw_list = [KEYWORD]
pytrends.build_payload(kw_list, cat=0, timeframe='today 5-y', geo='JP', gprop='')
trends = pytrends.related_queries()
trends_values = trends[KEYWORD]['top'].values.tolist()
```

## 追加补课 - 文字云

### 安装

```bash
$ pip install wordcloud
```

### main.py

```python
from collections import Counter
from wordcloud import WordCloud

# ---------- 出图设定 ----------
WORDCLOUD_FONT_PATH = './meiryob.ttc'
WORDCLOUD_WIDTH = 600
WORDCLOUD_HEIGHT = 600
WORDCLOUD_BG_COLOR = 'white'
WORDCLOUD_OUTPUT_FILE = './wordcloud.png'

word_counter = Counter(google_trend_list)
wordcloud = WordCloud(
    font_path = WORDCLOUD_FONT_PATH,
    width = WORDCLOUD_WIDTH,
    height = WORDCLOUD_HEIGHT,
    background_color = WORDCLOUD_BG_COLOR,
    colormap="summer").generate_from_frequencies(word_counter)
wordcloud.to_file(WORDCLOUD_OUTPUT_FILE)
```

## 课程文件

https://github.com/komavideo/KomaKnowledge

## 小马视频频道

http://komavideo.com

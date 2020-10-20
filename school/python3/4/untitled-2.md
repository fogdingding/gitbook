---
description: 字典的值可以有許多型態，也包含使用串列或是元組當成值。
---

# 字典值存在串列

#### 實驗室 1 - 三天的天氣記錄

```python
weather = { 'Temperature' : [30, 29, 25],
            'Humidity' : [65, 68, 95],
            'Weather' : ['晴朗', '多雲', '有雨']  }

print('第 2 天的天氣記錄：')
print('溫度\t' + str(weather['Temperature'][0]) + ' 度')
print('濕度\t' + str(weather['Humidity'][0]) + ' %')
print('天氣\t' + weather['Weather'][0])
```

以溫度為例，如果單純寫 `weather['Temperature']`，那就會輸出該鍵值，是一個串列 `[30, 29, 25]`；如果要更進一步取的該串列值內容，那就再加一個中括號上去存取該串列內容，就如同實驗室 1 所寫的 `weather['Temperature'][0]` 一樣。

由於已經是存取串列內容了，所以也同時適用於串列操作。




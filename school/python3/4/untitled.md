# 建立一個字典

建立字典是一件簡單的事，假若說今天這件商品有一些資訊，比如說：價格為 135 元、產地為台灣、生產年份為 2015 年，我們將透過字典去建立這些東西的記載，要如何做呢？

#### 實驗室 1 - 登記生產履歷

```python
product = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015}

print('價格\t' + str(product['price']))
print('原產地\t' + product['countryOfOrigin'])
print('生產年\t' + str(product['manufactureYear']))
```

我們使用大括號（`{}`）建立字典，每一個字典的元素都會有一個「鍵」（Key）還有「值」（Value）配對，形成一對的「鍵——值」（Key-Value）。

```python
product = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015}
```

我們將 `product` 字典變數拿出來看，會發現到：

1. `'price'` 這個鍵，會配對到 `135` 這個值
2. `'countryOfOrigin'` 這個鍵，會配對到 `'Taiwan'` 這個值
3. `'manufactureYear'` 這個鍵，會配對到 `2015` 這個值

彼此元素之間都以逗號（`,`）區隔，與串列元組沒有什麼兩樣。

當然，我們的鍵可以是數字形態，表達起來就跟串列相似了。


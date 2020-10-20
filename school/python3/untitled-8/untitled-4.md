# 使用 for 走訪字典內容

你會發現，Python 很多東西都很相似，在字典操作上與串列相似，那就代表`for` 對串列的操作幾乎可以整套搬過來這個單元上。

### 使用 `for` 走遍所有字典內容

當我們要把商品資訊從字典裡拉出來時，你鐵定不想要一個一個慢慢把鍵值打上去，你鐵定是想要叫 Python 用迴圈幫你做好這件事：

#### 實驗室 1 - 刊登商品列表

```python
product = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015}

for key, value in product.items():
  print(key + '\t' + str(value))
```

當要請 `for` 對整個字典做走訪時，你需要使用 `items` 這個方法產生出 `for` 迴圈可讀取的東西。

而 `for key, value in product.items():` 的 `key, value` 意思就是當每次執行一次迴圈時，`key` 會接住 `product.items()` 所產生的第一個東西（也就是鍵），而 `value` 會接住 `product.items()` 所產生的第二個東西（也就是值）。

因此，在輸出時，我們的 `print(key + '\t' + str(value))` 就會依序顯示出 `product` 字典變數的各項鍵值囉！

### 使用 `keys` 方法拿出字典的鍵

如果你只想拿出字典的鍵，而不想拿值，可以考慮使用 `keys` 方法：

#### 實驗室 2 - 取出商品屬性

```python
product = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015}

for key in product.keys():
  print(key)
```

此時你就會發現我們就只拿出 `product` 的鍵內容囉。

### 使用 `values` 方法拿出字典的值

如果你只想拿出字典的值，可以考慮使用 `values` 方法：

**實驗室 3 - 取出商品屬性**

```python
product = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015}

for value in product.values():
  print(value)
```












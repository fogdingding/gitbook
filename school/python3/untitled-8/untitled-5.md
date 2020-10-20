# 修改字典的鍵值配對

### 建立空字典

建立一道空字典，只需要將大括號（`{}`）指定給變數，就完成了。

#### 實驗室 1 - 建立空字典

```python
product = {}
print(product)
```

### 新增一些鍵值

我們可以使用類似於串列的方式進行鍵值的新增。

#### 實驗室 2 - 建立價格鍵值資料

```python
product = {}
product['price'] = 135
print(product)
```

執行實驗室 2 後發現，如果該鍵不存在於字典中，那麼就會新增該鍵值配對。

### 修改特定鍵值

我們可以使用類似於串列的方式進行鍵值的新增。

#### 實驗室 3 - 修改生產年份

```python
product = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015}

product['manufactureYear'] = 2018
print(product)
```

執行實驗室 3 後發現，如果該鍵存在於字典中，那麼就會修改該鍵的值內容。

### 刪除特定鍵值

使用 `del` 再搭上欲刪除的字典變數與鍵，就可以將該筆鍵值刪除。

#### 實驗室 4 - 刪除誤打的資料

```python
product = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015,
           'wowowow' : '?????'}

del product['wowowow']
print(product)
```








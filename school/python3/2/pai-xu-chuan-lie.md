# 排序串列

有時候我們需要將統計的資訊進行排序，比如說業績銷售量的排名等等；此時排序就是一個重要的議題。

### 使用 `sort` 永久排序串列

如果我們想將串列內的內容作永久排序，也就是說排序完無法回復原本順序時，可以使用 `sort` 方法來達成。

#### 實驗室 1 - 使用 `sort` 方法永久排序串列

```python
sales = [300, 200, 800, 900, 10]
sales.sort()
print(sales)
```

你會發現當經過 `sales.sort()`，再印出 `sales` 串列內容時，元素皆以被調動順序至排序好的位置了。

### 使用 `sorted` 暫時排序串列

若你單純只想暫時排序，但是不想更動原來的順序時；使用 `sorted` 函式是一個好主意：

#### 實驗室 2 - 使用 `sorted` 函式取得暫時排列的串列

```python
sales = [300, 200, 800, 900, 10]
print(sorted(sales))
print(sales)
```

當經過 `sorted(sales)` 時，你依然會發現輸出是排序好的串列；但是再次輸出 `sales` 時，就會發現還是原本的串列順序內容。

### 使用 `sort` 與 `sorted` 排序字串串列

當然，`sort` 與 `sorted` 排序不僅是數字，也可以是字串：

#### 實驗室 3 - 排序字串

```python
words = ['banana', 'zebra', 'apple', 'nail', 'nose']
print(sorted(words))
```

執行後，排序會以字母的順序進行調整；當然你也可以使用 `sort` 方法來達到永久排序。

### 使用 `reverse=True` 反過來排序

我們的排序似乎是從小到大的排序，如果可以反過來排序的話要如何做？

#### 實驗室 4 - 使用 `sort` 倒序排序

```python
sales = [300, 200, 800, 900, 10]
print(sales.sort(reverse=True))
print(sales)
```

在 `sort` 方法的括號內，使用 `reverse=True` 來達到反轉排序的效果；`reverse` 是一個參數名稱，後用一個 `True` 代表這個參數的值為「真」。

當然，我們也可以使用 `sorted` 倒序排序：

#### 實驗室 5 - 使用 `sorted` 倒序排序

```python
sales = [300, 200, 800, 900, 10]
print(sorted(sales, reverse=True))
print(sales)
```

與 `sort` 大同小異，在括號內，串列變數的後方加上 `reverse=True` 就可以達到這個效果。










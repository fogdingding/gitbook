# 複製串列

我們常常需要將一個串列複製出來作一些實驗操作；在不損及原始串列的內容下，這樣是最好的方式。  
在 Python 中，複製串列必須借用切片的概念，貿然使用等於指定，會有大麻煩：

#### 實驗室 1 - 【大麻煩】不用切片，以為複製了串列

```python
sales = [100, 400, 600, 300, 2000, 50, 300, 400, 500, 600, 700, 200]
salesSort = sales
salesSort.sort()

print(sales)
print(salesSort)
```

太不妙了，當執行 `salesSort.sort()` 進行串列排序時，居然 `sales` 也跟著動，這怎麼回事呢？

原來 Python 只是將 `sales` 牽一條捷徑給 `salesSort` 而非複製，所以 `salesSort` 有任何變動其實就是在改 `sales` 的內容。

如果要複製，兩個變數兩者彼此不互相影響該怎麼做呢？

#### 實驗室 2 - 複製串列

```python
sales = [100, 400, 600, 300, 2000, 50, 300, 400, 500, 600, 700, 200]
salesSort = sales[:]
salesSort.sort()

print(sales)
print(salesSort)
```

我們僅是將第 3 行從 `salesSort = sales` 改成 `salesSort = sales[:]`，使用切片時，Python 會確切的複製一份起來送到 `salesSort` 變數，這樣子，`salesSort` 有任何變動時，都不會影響到 `sales` 的變數囉。


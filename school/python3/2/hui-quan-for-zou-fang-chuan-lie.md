# 迴圈\(for\)走訪串列

我們可以使用 `for` 迴圈來走訪所有串列的內容，走訪串列內容這個技巧非常實用，假若你的串列內容需要進行統計分析，你將需要取得該串列的所有值；又或者是，將串列內的內容一一展示出來。

### `for` 走訪自訂串列

假若我們有五個人的業績，需要一一展示出來，可以使用 `for` 對該業績串列進行走訪，並一一輸出。

#### 實驗室 1 - 使用 `for` 走訪串列內容

```python
sales = [300, 200, 800]
for eachSale in sales:
  print(eachSale)
```

`for eachSale in sales:` 的意思是，將 `sales` 的元素內容一一的按順序丟進 `eachSale` 中。

執行第一次時，`for` 就會將 `sales[0]` 放進 `eachSale`；並執行 `print(eachSale)`

執行第二次時，`for` 就會將 `sales[1]` 放進 `eachSale`；並執行 `print(eachSale)`

執行第三次時，`for` 就會將 `sales[2]` 放進 `eachSale`；並執行 `print(eachSale)`

執行三次後，由於 sales 串列後續無東西，故停止執行。

> 特殊的是，你會發現 `for eachSale in sales:` 接下的指令是 `print(eachSale)` ，這道指令與上一道指令差了一個縮排（Indentation）；在 Python 中，縮排是重要的概念，他會協助 Python 了解哪一些指令是屬於哪一道指令之下；以此為例，`print(eachSale)` 是屬於 `for eachSale in sales:` 指令之下的內容。
>
> 每一個 `for` 寫完必須要有一個冒號（`:`）。

當然，我們可以使用 `for` 做更多的事情：

#### 實驗室 2 - 逐月展示業績

```python
sales = [100, 400, 600, 300, 2000, 50, 300, 400, 500, 600, 700, 200]
sum = 0
for eachSale in sales:
  print("該月銷售額：" + str(eachSale))
  sum += eachSale
  print("截至本月銷售額：" + str(sum))
```

每一個 `for` 中，只要縮排一致，就能執行多行的 `for` 內容；若執行 `for` 後，想再繼續執行指令，而非包在 `for` 中時，只要將該指令前的縮排拿除即可：

#### 實驗室 3 - 逐月展示業績，最後輸出總業績

```python
sales = [100, 400, 600, 300, 2000, 50, 300, 400, 500, 600, 700, 200]
sum = 0
for eachSale in sales:
  print("該月銷售額：" + str(eachSale))
  sum += eachSale
  print("截至本月總銷售額：" + str(sum))

print("總銷售額：" + str(sum))
```

你會發現，拿除縮排的 `print("總銷售額：" + str(sum))` 就不會在 `for` 中執行了。

### `for` 走訪整數串列

利用 `range` 函式可以產生一系列可供 `for` 使用的數字。

#### 實驗室 4 - 列印出 0 ~ 4 的數字

```python
for number in range(5):
  print(number)
```

`range(5)` 的意思等同於 `range(0,5)`，也就是從 0 開始，到 5 之前結束，每次加 1。

### `for` 走訪串列切片

串列切片出來還是一樣是一個串列，所以跟前面的 `for` 使用方法是類似的。

#### 實驗室 5 - 顯示夏季（5 ~ 8 月）的銷售額

```python
sales = [100, 400, 600, 300, 2000, 50, 300, 400, 500, 600, 700, 200]
sum = 0
for eachSale in sales[4:8]:
  print("該月銷售額：" + str(eachSale))
  sum += eachSale
  print("截至本月總銷售額：" + str(sum))

print("夏季總銷售額：" + str(sum))
```




























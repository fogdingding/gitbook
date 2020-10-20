# 存取串列

### 存取串列內容

串列的內容，或更精準地講，我們稱為「元素」（Element）；當我們想存取串列中的元素時，我們會將串列名稱後方加上中括號，中括號內填入想要取得元素的索引（Index）位置。

#### 實驗室 1 - 一個簡單的串列

串列（List）使用中括號（`[]`）括住多個內容，彼此的內容以逗號（`,`）區隔：

```python
fruits = ['apple', 'banana', 'pineapple']
print(fruits)
```

執行實驗室 1 時，我們會建立好 `fruits` 的串列結構，並執行輸出；此時，你會發現它將會輸出整個內容包含中括號 `['apple', 'banana', 'pineapple']`

#### 實驗室 2 - 使用索引取串列元素

```python
fruits = ['apple', 'banana', 'pineapple']
print(fruits[0])
print(fruits[1])
print(fruits[2])
```

經此，我們可以發現實驗室 2 依序輸出 `apple` 、 `banana` 與 `pineapple`；特別的是，串列第一個元素的索引值為 `0` ，並非直觀的 `1`，這點需要特別注意。

> 在python以及大部分程式語言的世界裡，對於串列的第一個元素通常會從`0`開始計算

Python 有許多神奇但直觀的用法，例如如何取得倒數第一個的串列元素？

#### 實驗室 3 - 使用索引值 `-1` 取得串列最後的值

```python
fruits = ['apple', 'banana', 'pineapple']
print(fruits[-1])
```

實驗室 3 可以得到 `pineapple` 的結果；以此類推，使用 `-2` 就可以取得 `banana`，使用 `-3` 就可以得到 `apple`。

假若我們以 `fruits = ['apple', 'banana', 'pineapple']` 來說，串列中的元素都是字串；因此也適用我們先前提及的字串操作，例如 `title`、`upper` 等等的。

#### 實驗室 4 - 串列元素是字串時的字串操作

```python
fruits = ['apple', 'banana', 'pineapple']
print(fruits[0].title() + ' is good!')
```

也是一樣，將字串後接上一個方法；亦可使用 `+` 進行字串連接。

### 使用 `len` 偵測串列長度

我們會需要取得串列的長度來計算資料筆數（總不會叫你一個一個慢慢算？）；這時，使用 `len` 函式是最適合的了！

#### **實驗室 5 - 計算串列元素個數（長度）**

```python
fruits = ['apple', 'banana', 'pineapple']
howManyFruits = len(fruits)
print('There are ' + str(howManyFruits) + ' fruits.')
```

在 `len` 的括號中填上欲計算長度的串列變數，即可取的該串列的元素總個數。

### 使用 `reverse` 反轉陣列內容

有時候我們會將串列倒序著看，有可能這個串列已經從小到大排好順序，我們想反轉串列讓他變成從大到小輸出；此時，我們可以使用 `reverse` 方法反轉。

#### **實驗室 6 - 使用 reverse 方法反轉串列**

```python
money = [400, 500, 600, 800, 10000]
money.reverse()
print(money)
```

經過 `reverse` 方法後，我們能夠發現整個串列都倒過來了。

### 存取不存在的串列元素

使用超過範圍的串列索引值會招致 Python 的怒火，他會很生氣的說「索引錯誤」（IndexError），此時你就必須要乖乖的把錯誤的索引值改正才能繼續進行。

#### 實驗室 7 - 【手賤特區】存取超過範圍的串列索引值

```python
money = [400, 500, 600, 800, 10000]
print(money[5])
```

實際上並沒有 `money[5]` 這玩意兒，最多才到 `money[4]` 而已，所以 Python 就會氣噗噗的說你這裡不對。此時，我們就必須把索引值進行修正`5` -&gt; `4` 才能正常的執行喔。

#### 實驗室 8 - 存取範圍內的串列索引值

```python
money = [400, 500, 600, 800, 10000]
print(money[4])
```

實際上並沒有 `money[5]` 這玩意兒，最多才到 `money[4]` 而已，所以 Python 就會氣噗噗的說你這裡不對。








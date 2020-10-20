# 修改串列

很多時候，我們都會需要動態調整串列的內容；比如說你正在收集一些資料，總不能寫死在那邊而不能變更資料；因此，當我們新建一個串列結構，希望可以動態的去更改他。

### 修改元素

修改資料是天經地義的事，總不能寫錯資料還改不了；我們若要改變串列內容，指定欲改變的串列索引值，再給予新值即可達成這個目的。

#### 實驗室 1 - 修改串列資料

```python
temperature = [24, 25, 24, 27, 29]
temperature[0] = 20
print(temperature)
```

假若串列是每日溫度的資料值，在這邊，我們將 `temperature[0]` 指定新的值為 `20`，輸出時也確實被修改了。

### 使用 `append` 新增元素

假若串列是每日溫度的資料值，當有新的資料進來時，必定需要新增新的資料到串列中；此時，我們會使用 `append` 的方法將元素新增至串列的尾端。

#### 實驗室 2 - 使用 `append` 新增資料

```python
temperature = [24, 25, 24, 27, 29]
temperature.append(30)
print(temperature)
```

`append` 括號內放上你需要加到串列尾端的內容；當你執行實驗室 5 的時候，你就會發現 `temperature` 已經新增新值 `30` 在串列尾端了。

### 使用 `insert` 插入元素

有時候我們發現有一些串列中間可能少了一筆資料，因此我們需要利用 `insert` 指定我們的值要放在哪個位置。

**實驗室 3 - 使用 insert 插入資料**

```python
temperature = [24, 25, 24, 27, 29]
temperature.insert(3, 30)
print(temperature)
```

`insert` 內部第一個引數是指定我要把新值放在哪個位置，第二個引數代表我的新值的值為何；在此，我們是要將 `30` 這個值放入 `temperature[3]` 的地方，原本的 `temperature[3]` 與往後的值都會右移一格。

### 使用 `pop` 提取並刪除元素

單純使用 `pop` 可將串列最後一個元素提取出來，並刪除。

#### 實驗室 4 - 使用 `pop` 彈出最後一筆資料

```python
temperature = [24, 25, 24, 27, 29]
getLatestTemperature = temperature.pop()
print('Recent Temperature: ' + str(getLatestTemperature))
print(temperature)
```

`pop` 會將 `temperature` 串列尾端的元素提取出來（也就是 `29`），而這個元素也將會從 `temperature` 彈出消失。

如果想要提取並刪除某一個指定元素，就必須將 `pop` 的括號內填上該陣列索引值。

#### 實驗室 5 - 使用 `pop` 彈出特定資料

```python
temperature = [24, 25, 24, 27, 29]
getFourthTemperature = temperature.pop(3)
print('Fourth Day Temperature: ' + str(getFourthTemperature))
print(temperature)
```

此時，我們的 `pop` 就會將 `temperature` 的索引 3 的值取出，並刪除。

### 使用 `del` 刪除元素

新增資料必定也有刪除資料的可能性；我們可以利用 `del` 陳述句進行特定元素的刪除。

#### 實驗室 6 - 刪除特定元素

```python
temperature = [24, 25, 24, 27, 29]
del temperature[3]
print(temperature)
```

`del` 後面接著你想要刪除的串列名稱以及元素索引值；在此，我們是刪除 `temperature[3]` 的元素，也就是 `27`。

> 使用 `del` 刪除元素時，就是直接刪除，並不會將值提取出來供使用。






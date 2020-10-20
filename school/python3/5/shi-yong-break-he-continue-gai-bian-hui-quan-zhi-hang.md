# 使用 break 和 continue 改變迴圈執行

### `break`

跳離迴圈除了讓 `while` 不符合執行條件外，也是可以使用 `break` 讓迴圈強制跳離；當執行到 `break` 時，`break` 以下到迴圈包覆的範圍都一概不執行了，直接跳出迴圈。

#### 實驗室 1 - 我的完美記帳簿——第二版

```python
myMoney = []
currentMoney = 0
totalMoney = 0
while currentMoney != -1:
  currentMoney = int(input('請輸入金額，若要停止請輸入 -1：'))

  if currentMoney == -1:
    break

  myMoney.append(currentMoney)
  totalMoney += currentMoney

print("總金額為：" + str(totalMoney))
```

當你輸入 `-1` 時，就會啟動 `if currentMoney == -1:` 並執行 `break`，以下的迴圈程式碼都不執行，直接跳離。

### `continue`

`continue` 還是會讓迴圈繼續執行，但是一旦執行到 `continue` 的時候，他會跳過 `continue` 以下的迴圈執行內容，重新開始新的迴圈：

#### 實驗室 2 - 輸出 8 到 99 之間不能被 3 整除的數字

```python
num = 8

while num < 99:
  num += 1
  if num % 3 == 0:
    continue
  print(num)
```

你會發現說，當 `num` 整除 `3` 時（也就是餘數為 `0`）時，就會啟動 `if num % 3 == 0:` 執行 `contine`，接下來就會省略過該次的 `print(num)` 並直接重啟一個新的迴圈。




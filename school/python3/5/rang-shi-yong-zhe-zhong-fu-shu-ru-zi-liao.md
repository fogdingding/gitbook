# 讓使用者重複輸入資料

我們知道使用 `input` 函式可以從輸入裝置讀取使用者鍵入的資料，但是這只能輸入一次；在此，我們可以使用 `while` 迴圈重複讀取使用者輸入資料。

#### 實驗室 1 - 我的不完美記帳簿

```python
myMoney = []
currentMoney = 0
totalMoney = 0
while currentMoney != -1:
  currentMoney = int(input('請輸入金額，若要停止請輸入 -1：'))
  myMoney.append(currentMoney)
  totalMoney += currentMoney

print("總金額為：" + str(totalMoney))
```

你發現了嗎？每次我輸入完離開時都會少一塊錢，這是因為當我輸入 `-1` 的時候是在迴圈當中，他勢必還會執行一次 `myMoney.append(currentMoney)` 以及 `totalMoney += currentMoney` 所以就會被扣掉一塊錢。

因此，我們需要加入一些判斷，讓他避免掉這種誤加的狀況：

#### 實驗室 2 - 我的完美記帳簿

```python
myMoney = []
currentMoney = 0
totalMoney = 0
while currentMoney != -1:
  currentMoney = int(input('請輸入金額，若要停止請輸入 -1：'))
  if currentMoney != -1:
    myMoney.append(currentMoney)
    totalMoney += currentMoney

print("總金額為：" + str(totalMoney))
```

執行後，當你再次輸入 `-1` 時，`if currentMoney != -1:` 就會發揮功效，阻擋 `-1` 進入 `myMoney` 以及 `totalMoney` 之中；因此，你的總額出來就會是正確的。


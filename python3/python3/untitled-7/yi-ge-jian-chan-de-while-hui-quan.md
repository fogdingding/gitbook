# 一個簡單的 while 迴圈

`while` 迴圈接上一個條件式，當條件式為 `True`，那就開始啟動迴圈，每執行一次迴圈都會檢查一次條件式的狀態，直到條件式為假時才會終止執行。

#### 實驗室 1 - 讓 `while` 迴圈執行 10 次

```python
count = 1
while count <= 10:
  print(count)
  count += 1
```

實驗室 1 的 `while count <= 10:`，代表著當 `count <= 10` 為 `True` 時，就會進入到 `while` 中執行；輸出目前的 `count` 值後，就會接著執行 `count += 1` 把變數值加 1 上去。

這樣執行 10 次後，`count` 變數就會來到 `11`；此時，再次檢查 `count <= 10` 時就會變成 `False`，`while` 就會停止執行，並繼續往下執行其他指令。


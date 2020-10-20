# 縮排（Indentation）



縮排（Indentation）在 Python 語言中扮演極具重要的角色，Python 根據該指令的縮排個數來決定這行指令究竟是屬於誰的；不一致的縮排可能會導致 Python 程式執行不如預期或是發生錯誤。

### 縮排的規定

縮排規格必須一致，這是縮排規定的中心思想

1. 如果使用 Tab 排版，必須以 Tab 縮排到底；若以空白排版，必須以空排縮排到底。
2. 使用縮排時，縮排的間隔長度必須一致，若是使用 2 個空白為一個縮排單位，那你不可以下一句使用 3 個空白。

#### 實驗室 1 - 一個正常的縮排

```python
sales = [300, 200, 800]
sum = 0
for eachSale in sales:
  print("該月銷售額：" + str(eachSale))
  sum += eachSale
  print("截至本月總銷售額：" + str(sum))

print("總銷售額：" + str(sum))
```

以上示範是一個正常使用的縮排，非常一致。

#### 實驗室 2 - 【手賤特區】Tab 與 空白混用

> _複製貼上時，需要手動更換空白與 tab_
>
> 請點入互動式教材

```python
sales = [300, 200, 800]
sum = 0
for eachSale in sales:
  print("該月銷售額：" + str(eachSale))
  sum += eachSale
  print("截至本月總銷售額：" + str(sum))

print("總銷售額：" + str(sum))
```

這種不一致的縮排混用會造成縮排錯誤（IndentationError）。

#### 實驗室 3 - 【手賤特區】不一致的縮排長度

```python
sales = [300, 200, 800]
sum = 0
for eachSale in sales:
  print("該月銷售額：" + str(eachSale))
   sum += eachSale
   print("截至本月總銷售額：" + str(sum))

print("總銷售額：" + str(sum))
```

我們會發現，這種不一致的縮排也會造成縮排錯誤（IndentationError）。

### 縮排使用的時機

最後，我們將告訴您：基本上只要遇到冒號（`:`），基本上就會需要進行縮排。  
然而，縮排的結束，也就是跟 （`:`） 相關的程式碼結束即可將縮排結束。如實驗室 1的第三行（縮排開始）、第六行（縮排）以及第八行（結束縮排）的關西。




















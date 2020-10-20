---
description: 只要是大於一個字的，都稱為「字串」（String）（單個字，稱為字元 Character）。
---

# 字串

### 字串解說

`Hello, Word!` 這一串字，都稱為「字串」（String），而 `H` 、 `e`  這些單個字稱之為字元（ Character）

在 Python 中，字串可以用單引號（`''`）或是雙引號（`""`）括起來；因此，可以視情況彈性的使用。

### 實驗室 - 字串訓練

#### 實驗室 - 利用 `title` 將每個詞的首字轉為大寫

今天給定一個詞 `hello word!` ，想要把每個詞的首字改為大寫（也就是把 `h` 改為 `H`），那可以使用 `title` 方法（method）進行更換

```text
text = "hello word!"
print(text.title())
```

我們將字串`hello word!`放入變數`text`裡面。我們就會有一個字串型態的變數，而這個變數就會有許多方法\(method\)可以使用。

#### 實驗室 - 利用 `upper` 將所有字轉為大寫

今天給定一個詞 `hello word!` ，想要把每個字改為大寫（也就是變成 `HELLO WORD!`），我們使用 `upper` 方法（method）進行更換

```python
text = "hello word!"
print(text.upper())
```

#### 實驗室 - 利用 `lower` 將所有字轉為小寫

今天給定一個詞 `HELLO WORD!` ，想要把每個字改為大寫（也就是變成 `hello word!`），我們將使用 `lower` 方法（method）進行更換

```python
text = "HELLO WORD!"
print(text.lower())
```

### 實驗室 - 字串連接訓練

有時候我們會將兩個字並在一起使用，例如：在網站上你常常在註冊時，會將姓氏與名字分開來寫；進到網站後發現系統把這名字合在一起顯示，這裡很有可能使用字串連接的方法。

在 Python 中也有字串連接（Concatenate）的方法，用非常直觀的 `+` 作為字串連接。

#### 實驗室 - 利用 `+` 將字串做連接

```python
name = 'GAIS'
welcomeMessage = '歡迎!'
print(welcomeMessage + ", " + name)
```

在上面的`實驗室 - 利用 + 將字串做連接`，我們成功使用 `+` 將三個字串做連接，並顯示出 `歡迎, GAIS` 這個訊息。  
當然，我們也可以把這些訊息一起放進變數中：

#### 實驗室 - 利用 `+` 將字串做連接2

```python
name = 'GAIS'
welcomeMessage = '歡迎'
wholeMessage = welcomeMessage + ", " + name
print(wholeMessage)
```

### 實驗室 - 特殊符號

使用多道 `print` 指定可以將不同的字串分行印出；若是只限定用一道 `print` 指令，卻想要換行，該怎麼辦呢？

#### 實驗室 - 利用  `\n`  換行

使用 `\n` 這個字元（沒錯，這個叫跳脫字元，由一個反斜線及一個字元組成），可達成換行的目的：

```python
print("Hello, Word!\nHello, Python3!")
```

#### 實驗室 - 利用  `\t`  排版

tab 符號又稱定位符號；在程式表示上為 `\t`，我們常使用 tab 符號進行排版

```python
print("Language:\tC\tPython")
print("Less Code?\tNo\tYes")
```

當你執行時會驚訝說，利用 tab 排版其實非常實用；在不同字數之間取得一個巧妙的空白平衡。

### 實驗室 - 利用  `strip rstrip lstrip`  刪除多餘的空白

在分析資料時，我們常常將空白捨去，以節省程式空轉或是出錯的機會；例如說，我們有兩個人名：`GAIS` 和 `GAIS`  ，你肉眼就能知道，這兩個人是一樣的名字，但是對於程式語言來說，因為兩個字串並不一樣（後者多了空白），導致在判斷時不符預期；這時就需要刪除多餘的空白，我們也稱這個手續為「資料前處理」。

我們可以使用 `strip` 、 `rstrip` 、 `lstrip` 方法，進行空白字元刪除。

#### 實驗室 - 刪除右側結尾空白字元

```python
text = "今天天氣晴時多雲     "
print(text.rstrip())
```

#### 實驗室 - 刪除左側開頭空白字元

```python
text = "     今天天氣晴時多雲"
print(text.lstrip())
```

#### 實驗室 - 刪除兩側空白字元

```python
text = "     今天天氣晴時多雲     "
print(text.strip())
```

使用到這裡，你可能會認為同時使用 `rstrip` 與 `lstrip` 可以達成 `strip` 的功效；在某個程度上這是對的，那要看你如何使用。

#### 實驗室【手賤特區】 - `rstrip` 與 `lstrip` 無法達成 `strip` 效果

```python
text = "     今天天氣晴時多雲     "
print(text.rstrip())
print(text.lstrip())
```

你會覺得奇怪，為何經過 `rstrip` 再經過 `lstrip` 後本應該兩側空白清空，為何還是變成左側空白清空而已？

其實使用這些方法時，它並不會更動原來變數的內容，你必須將方法使用後，把新的值複寫回變數值才可以達到目的喔！

#### 實驗室  - 使用 `rstrip` 與 `lstrip` 達成 `strip` 效果

```python
text = "     今天天氣晴時多雲     "
print(text.rstrip())
text = text.rstrip()
print(text.lstrip())
```

多虧了 `text = text.rstrip()` 這行可以將刪除右側空白後的字串存回 `text` 變數；這時再使用 `lstrip` 就可以將兩側空白清空了！

### 實驗室 - 單引號與雙引號的使用時機

我們在最早的時候，提到說可以使用單引號以及雙引號來刮起字串

#### 實驗室 - 一個平凡的字串

```python
text = "GAIS's bag is cool!"
print(text)
```

這邊使用雙引號是可以執行的，但是如果換成單引號就會有點麻煩了。

#### 實驗室【手賤特區】 - 一個不平凡的字串

```python
text = 'GAIS's bag is cool!'
print(text)
```

Python 會跳出語法錯誤（SyntaxError）警告，原因是因為我們括住的字串所使用無論單引號還是雙引號也好，都需要成雙成對； `實驗室【手賤特區】 - 一個不平凡的字串`的字串的 `Gary's` 的單引號提前與括住字串的單引號配對了，導致後面的字串找不到單引號配對，形成孤兒。

因此，彈性使用雙引號與單引號或是使用字串連接就可以避免這個問題了。












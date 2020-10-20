# if 陳述句

`if` 這個字，中文來說就是「如果」的意思，後面跟隨著一串條件式，若成立就會執行 `if` 以下內容：

#### 實驗室 1 - 簡單的 `if` 陳述句

```python
username = 'Juice'
if username == 'Juice':
  print('Welcome Juice!')
  print('How are you today?')
```

在此，我們發現 `username` 確實與 `Juice` 字串相同，那麼就會執行 `print('Welcome Juice!')` 以及 `print('How are you today?')` 這兩串字。

在字串比對時，要完全一致，如果 `juice` 與 `Juice` 相比，那絕對是不同的，因為第一個字大小寫不一致。

我們在做系統的時候，常需要對登入帳號的身分進行判斷，給予不同的權限，這通常也是使用 `if` 來達成的：

#### 實驗室 2 - 判斷是否為超級使用者

```python
id = 0
username = 'admin'

if id == 0 and username == 'admin':
  print('You are admin!')
```

在實驗室 2 中，我們用複合條件式檢驗，如果 `id` 為 `0` 而且 `username` 又是叫做 `admin` 時，那就輸出 `You are admin!`。


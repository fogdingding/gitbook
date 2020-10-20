# 變數概觀

### 變數入門

如果說我們要印出 5 個 `Hello, GAIS!`，那麼最直觀的方法就是把 `print("Hello, GAIS!")` 複製個五遍，就可以了。

#### 實驗室 1 - 印出 5 個 Hello, GAIS!

```python
print("Hello, GAIS!")
print("Hello, GAIS!")
print("Hello, GAIS!")
print("Hello, GAIS!")
print("Hello, GAIS!")
```

但是，有一天我們卻需要把 GAIS 這個字改成 Python，這就麻煩了，你需要改五次；這時候，我們可以使用「變數」（Variables）來改善我們的作業流程。

#### 實驗室 2 - 將 Hello, Juice! 存進變數中

```python
text = "Hello, Word!"
print(text)
print(text)
print(text)
print(text)
print(text)
```

每個變數都會有他的名字以及他的值，像在實驗室 2 ，我們宣告了一個名字叫 `text` 的變數，裡面放了 `"Hello, Word!"` 這個字串的值。

只要把 `text` 這個變數的名子放進 `print` 中，`print` 就會把變數裡面的值拿出來，輸出在螢幕上。

執行完實驗室 2 後，不錯，這次也順利達成印了 5 次 `Hello, Word!`；這時，你只需要在變數 `text` 裡頭把 `Word` 改成 `Python` 就可以了，不需要改五次。



#### 實驗室 3 - 將 Hello, Juice! 改成 Hello, Python!

```python
text = "Hello, Python!"
print(text)
print(text)
print(text)
print(text)
print(text)
```

### 變數的命名

幫變數取名字是需要花一些心思的，就如同為自己心愛的寵物或是小孩取名一樣；但是在 Python 的世界中，取名字需要遵循這個世界的規則，否則Python是無法認識您所取的名稱。

1. 變數名稱僅能使用英文字母、數字、底線。
2. 變數名稱不可以以數字開頭。
3. 變數名稱中不可以含有空白。
4. 變數名稱不可以使用 Python 關鍵字（保留字）及內建函式的名稱。

#### Python 的關鍵字（Keywords）

```python
False      await      else       import     pass
None       break      except     in         raise
True       class      finally    is         return
and        continue   for        lambda     try
as         def        from       nonlocal   while
assert     del        global     not        with
async      elif       if         or         yield
```

> 變數名稱建議最好是使用有意義的名稱；例如變數 `saturdayMoney`，別人在閱讀或是自己日後除錯維護時，就能快速掌握這個變數大致作用為何。

**實驗室 4 - 【手賤特區】打錯變數名稱**

有時候，在打 Python 程式時，偶爾會打錯字，導致執行異常：

```python
text = "Hello, Python!"
print(txt)
```

這時，Python 就會以 `NameError` 的錯誤訊息，警告我們在 `print(txt)` 內部的 `txt` 變數並未宣告；當然，我們並不是要宣告這個變數，而是少打了 `e`。














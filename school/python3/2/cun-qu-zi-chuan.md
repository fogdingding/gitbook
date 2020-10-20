# 存取字串

一連串的字元可以形成字串，我們也可以利用類似串列元組的方式存取字串：

#### 實驗室 1 - 查看這串字的第 1、2、3 個字

```python
string = 'Wow, so cool.'
print(string[0])
print(string[1])
print(string[2])
```

但是 Python 字串擁有不可變更的性質（Immutable），因此不可以將字串中某一個字進行調整：

#### 實驗室 2 -【好奇寶寶】更改字串中某一個字

```python
string = 'Wow, so cool.'
string[0] = '?'
print(string[0])
```

這個行為會招致 Python 跳出 TypeError 錯誤，並告訴你 `str` 也就是「字串」並沒有指定資料的方法可供使用。

### 利用 `len` 函式計算字數

由於類似於串列元組的存取方式，我們也可以使用 `len` 計算字數：

#### 實驗室 3 - 查看這串字的字數

```python
string = 'Wow, so cool.'
print(len(string))
```

### 利用 `for` 存取字串

#### 實驗室 4 - 逐字印出

```python
string = 'Wow, so cool.'
for character in string:
  print(character)
```




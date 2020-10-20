---
description: Python 有許多轉型的方法，所謂轉型，就是將某一個型態轉換為另外一種型態。
---

# 基本轉型

### 整數轉型

使用 `int` 函式，將任何數字，或是合適的字串轉換為整數。

#### 實驗室 1 - 浮點數轉整數

```python
number = 5.4
print(int(number))
```

小數轉整數會將小數部分截斷取整數。

#### 實驗室 2 - 合適的字串轉整數

```python
numberString = '8'
print(int(numberString))
```

若字串是純數字字元組成，就可進行轉換。

何謂「不合適的字串」？

#### 實驗室 3 - 含有非數字字元的字串轉整數

```python
illegalString = 'abc'
print(int(illegalString))
```

這會使得 Python 舉出 `ValueError` 的錯誤。

另外使用 `int` 轉型浮點數樣式的字串也會發生同樣錯誤：

#### 實驗室 4 - 含有浮點數字樣的字串轉整數

```python
illegalFloatString = '10.8'
print(int(illegalFloatString))
```

### 浮點數轉型

使用 `float` 函式，將任何數字，或是合適的字串轉換為浮點數。

#### 實驗室 5 - 整數轉浮點數

```python
number = 5
print(float(number))
```

#### 實驗室 6 - 合適的字串轉浮點數

```python
numberString = '8'
print(int(numberString))
```

若字串是浮點數樣式字元組成，就可進行轉換。

何謂「不合適的字串」？

#### 實驗室 7 - 含有非浮點數樣式字元的字串轉整數

```python
illegalString = '5.a'
print(int(illegalString))
```

### 字串轉型

使用 `str` 函式，將其他型態轉為字串表示方法。

#### 實驗室 8 - 整數轉字串

```python
number = 5
print(str(number))
```

#### 實驗室 9 - 浮點數轉字串

```python
number = 5.8
print(str(number))
```






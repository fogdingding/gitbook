# 建立一個例外

#### 實驗室 1 - 例外拋出

```python
print(8/0)
```

#### 實驗室 2 - 建立一個例外處理

```python
try:
    print(8/0)
except ZeroDivisionError:
    print("QQ, 除數是0")
```

這樣在遇到除數為零的時候，我們就可以告知python這時候應該要怎麼處理。


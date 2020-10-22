# 自定義的例外

### 自定義例外1

#### 實驗室 1 - 例外套件

```python
import builtins
print(dir(builtins))
```

我們可以看到有許多已經定義好的例外

#### 實驗室 2 - 建立一個自定義的例外

```python
import builtins


class OtherError(Exception):
    pass
```

沒錯，就是這麼簡單。 只需要建立一個`Class`並繼承`Exception`即可唷～

#### 實驗室 3 - 測試自定義例外

```python
import builtins


class OtherError(Exception):
    pass

try:
    raise OtherError('raise actively', 'user-defined exception example')
except OtherError as e:
    print(e)
```

當我們在`try`...`except`內，在想要拋出例外訊息的地方使用`raise`以及我們定義好的例外就可以順利拋出了喔。

### 自定義例外2

當然，聰明的你一定已經發先，既然他是一個`Class`，那我是不是可以應用之前所學的東西來去編輯他的呢？

#### 實驗室 4 - 編輯自定義例外

```python
import builtins


class OtherError(Exception):
    def __init__(self, cause, message):
        super().__init__(cause, message)
        self.cause = cause
        self.message = message
    def __str__(self):
        return self.cause + ' : ' + self.message

try:
    raise OtherError('raise working', 'OtherErrorTest')
except OtherError as e:
    print(e)
    print(e.cause + " > " + e.message)
    print(e.args[0] + " >> " + e.args[1])
```

成功後會輸出以下字串。 raise working : OtherErrorTest raise working &gt; OtherErrorTest raise working &gt;&gt; OtherErrorTest 我們應該可以看到，不僅例外成功的自定義，也成功的使用例外`Class`了哦～


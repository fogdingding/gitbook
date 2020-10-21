# 建立一個類別



在建立類別的時候，我們會需要先對他的屬性做一個定義; 換句話就是說，汽車的模版需要哪些資訊呢？（汽車姓名、顏色、重量等）

#### 實驗室 1 - 一個定義的函式

```python
class Car():
    '''a simple attempt to momdel a car'''
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight'''
        self.kind = kind
        self.color = color
        self.weight = weight

GAIS = Car("GAIS", "white", "1.5")
School = Car("School", "red", "2.0")

print(GAIS.kind, GAIS.color, GAIS.weight)
print(School.kind, School.color, School.weight)
```

在建立完成後，我們可以透過印出實例物件內的一些資訊，來確保我們有成功建立了。

### `__init__`???

**init** 為 python對於`Class`的保留字，主要是讓這一個類別能夠存取一些由我們定義的屬性\(`資料`\)。 也就是說，從實驗室1，我們在要建立實例物件的時候，需要在裡面放入 `kind` ， `color` 和 `weight` 三個屬性資料。 未來我們就能在這個地方去做一些存取的動作。

> 記得在每一個類別內的函式加入`self` 參數，這是用來讓類別跟自己溝通所需要的參數。


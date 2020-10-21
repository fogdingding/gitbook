# 修改屬性



在上一單元我們介紹了如何建立一個類別。 今天汽車製造老闆說：`GAIS-Car`的重量調高一些，這樣開起來才會穩。換句話說，我們需要針對實例進行修改屬性的部分。這時候我們應該怎麼做呢？

### 建立實例與修改

#### 實驗室 1 - 修改屬性

```python
class Car():
    '''a simple attempt to momdel a car'''
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight'''
        self.kind = kind
        self.color = color
        self.weight = weight

    def change_weight(self, weight):
        self.weight = weight

# 修改前
GAIS = Car("GAIS", "white", "1.5")
print(GAIS.kind, GAIS.color, GAIS.weight)
# 修改後
GAIS.change_weight("1.6")
print(GAIS.kind, GAIS.color, GAIS.weight)
```

在實驗1的時候，我們透過類別內的 `change_weight` 函式去做修改。當然我們也能提供其他函式來繼續修改其他屬性資料

#### 實驗室 2 - 修改屬性2

```python
class Car():
    '''a simple attempt to momdel a car'''
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight'''
        self.kind = kind
        self.color = color
        self.weight = weight

    def change_color(self, color):
        self.color = color

    def change_weight(self, weight):
        self.weight = weight

# 修改前
GAIS = Car("GAIS", "white", "1.5")
print(GAIS.kind, GAIS.color, GAIS.weight)
# 修改後
GAIS.change_color("red")
GAIS.change_weight("1.6")
print(GAIS.kind, GAIS.color, GAIS.weight)
```

### 類別與實例物件的衝突？

#### 實驗室 3 - 實例物件衝突？

```python
class Car():
    '''a simple attempt to momdel a car'''
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight'''
        self.kind = kind
        self.color = color
        self.weight = weight

    def change_color(self, color):
        self.color = color

    def change_weight(self, weight):
        self.weight = weight

# 修改前
GAIS = Car("GAIS", "white", "1.5")
School = Car("School", "white", "1.5")
print(GAIS.kind, GAIS.color, GAIS.weight)
print(School.kind, School.color, School.weight)

# 修改後
GAIS.change_color("red")
GAIS.change_weight("1.6")
print(GAIS.kind, GAIS.color, GAIS.weight)
print(School.kind, School.color, School.weight)
```

在實驗室3，我們透過 `Car` 類別來實例化兩個物件\(`GAIS`和`School`\)。 並針對`GAIS`來進行屬性修改。 再來我們對`GAIS`進行修改後，印出`GAIS`和`School`。我們可以發現，`GAIS`已經順利修改了資訊，而且並不會影響`School`的資訊。

> `Class` 可以透過實例建立許多物件，而物件可以透過物件內自定義的函式進行屬性修改或功能; 其中物件1與物件2兩者是毫無相關的\(除了他們的模板都是`Car`類別之外\)。


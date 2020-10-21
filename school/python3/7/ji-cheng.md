# 繼承

在對類別與物件有了一定程度的了解之後，我們就要來談談繼承\(inheritance\)了 在我們設計類別的時候，不一定每次都要重頭開始，如果我們要編寫的類別跟另一個很相似，就可以使用繼承\(inheritance\)的方式來製作。 什麼意思呢？？ 今天老闆說：我覺得我們在傳統的汽車上已經建置部署的差不多了，我想要往電動車的方向邁進。 換句話說，我們在之前已經有了一個設計好的`Car`類別，而傳統汽車跟電動車的差異; 就是電動車其實也是在`Car`底下的另一種分支; 換句話說就是，`Car`是父親一樣的類別\(superclass\)，而`ElectricCar`就像兒子一樣的類別\(subclass\)。 因此我們將會教導大家使用繼承，透過繼承`Car`類別來製作新的`ElectricCar`類別。

#### 實驗室 1 - 繼承類別？

```python
# 之前建立好的Car類別
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

# 繼承Car的ElectricCar類別

class ElectricCar(Car):
    '''represent aspects of a car(Class), to crect electric_car(Class)'''
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight, from superclass(Car)'''
        super().__init__(kind, color, weight)

E_Car = ElectricCar("E-Car", "white", "1.0")
print(E_Car.kind, E_Car.color, E_Car.weight)
```

由實驗室1的範例，我們成功的創立一個`ElectricCar`類別是由`Car`繼承而來的。 這當中我們使用一個特別的函式來替我們處理子類別\(subclass, `ElectricCar`\)與父類別\(superclass, `Car`\)當中連接起來的部分。

### 子類別修改屬性或功能使用？

#### 實驗室 2 - 子類別的操作

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

class ElectricCar(Car):
    '''represent aspects of a car(Class), to crect electric_car(Class)'''
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight, from superclass(Car)'''
        super().__init__(kind, color, weight)
        self.power = "Electric"
    def return_power(self):
        return self.power

E_Car = ElectricCar("E-Car", "white", "1.0")
print("this car's power is " + E_Car.return_power())
```

透過實驗室2的範例，我們成功的撰寫了一個屬於子類別\(subclass, `ElectricCar`\)的函式`print_power`來做操作。

### 覆蓋父類別的函式

#### 實驗室 3 - 覆蓋父類別的函式

在父類別\(superclass, `Car`\)中新增一個函式，fill\_up\(\)。

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

    def change_weight(self, weight):
        self.weight = weight

    def fill_up(self):
        print("this car need to fill up!")

class ElectricCar(Car):
    '''represent aspects of a car(Class), to crect electric_car(Class)'''
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight, from superclass(Car)'''
        super().__init__(kind, color, weight)
        self.power = "Electric"
    def return_power(self):
        return self.power

E_Car = ElectricCar("E-Car", "white", "1.0")
E_Car.fill_up()
```

#### 實驗室 4 - 覆蓋父類別的函式2

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

    def change_weight(self, weight):
        self.weight = weight

    def fill_up(self):
        print("this car need to fill up!")

class ElectricCar(Car):
    '''represent aspects of a car(Class), to crect electric_car(Class)'''
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight, from superclass(Car)'''
        super().__init__(kind, color, weight)
        self.power = "Electric"
    def return_power(self):
        return self.power

    def fill_up(self):
        print("this car not need to fill up!")

E_Car = ElectricCar("E-Car", "white", "1.0")
E_Car.fill_up()
```

透過實驗3和4，我可以發現`E_Car.fill_up()`執行輸出的字串已經改變了。因此如果我們想要修改父類別\(superclass, `Car`\)當中的函式，我們只需要名稱相同即可; python就會不去看父類別的函式。


# 修改繼承

在上一個單元我們對於繼承已經有一定的了解了。 但是有時候我們可能不需要父類別\(superclass, `Car`\)當中的某一個函式，甚至我們想要去做修改功能的部分。這時候我們應該怎麼做呢？

### 覆蓋父類別的函式

#### 實驗室 1 - 覆蓋父類別的函式

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

在實驗室1的時候，我們所執行`fill_up()`印出來的是在父類別\(superclass, `Car`\)中的一個函式，fill\_up\(\)。

#### 實驗室 2 - 覆蓋父類別的函式2

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


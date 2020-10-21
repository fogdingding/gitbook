# 類別的風格

### 風格

1. 類別的命名方式是採用駝峰式\(CamelCaps\)的命名方式，其作法是在類別取名的時候，相連每一個字詞，並在每個字詞的第一個字母做大寫來命名。
2. 定義類別的下一行，來添加註解。
3. 可以用空行來組織程式碼間的區隔編排，但是不要濫用，通常以一行來進行分隔。

#### 實驗室 1 - 函式的風格

```python
# 第一點，採用駝峰式命名
class ElectricCar():
    # 第二點，添加註解
    '''a simple attempt to momdel a ElectricCar'''

    # 第三點，透過空行來進行編排區塊程式碼的部分
    def __init__(self, kind, color, weight):
        '''initialize kind, color and weight'''
        self.kind = kind
        self.color = color
        self.weight = weight
```

> 這件事情並沒有強制規範，換句話說就算不符合也能夠執行。但是還是希望大家能夠持有這項優良的習慣！ 下面資料來源有提供相關的更詳細的程式碼編寫規則

### 資料來源

[python-PEP8](https://www.python.org/dev/peps/pep-0008/)


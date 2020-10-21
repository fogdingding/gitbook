# 參數和引數

執行完上一單元的程式碼後，我們就可以有一個自己的函式，但是還沒解決之前我們所說的，想印出不同的字串該怎麼做呢？ 別急，讓我來一步一步解釋。這時候我們就要提到，引數以及參數了。

#### 實驗室 1 - 參數和引數

```python
def lab_print(parameter):
    print("Hello" + parameter)

argument = "GAIS"
lab_print(argument)
```

我們替這個實驗命名了兩個變數分別為parameter和argument。首先定義在函式上的變數，我們稱之為參數，也就說我們將會提供這個函式一個參數讓他能夠進行某些工作。 而在呼叫函式並給參數的時候，這個變數我們稱之為引數。

> 大部分的人引數跟參數其實沒有分的那麼清楚，有時候還會把兩個詞互換介紹。參數內的變數稱之為引數，呼叫並給予函數的變數稱之為參數。

### 引數的傳導

再把引數丟入函式的時候，我們有兩種方法，分別為位置引數和關鍵字引數。 位置引數：透過與函式的參數位置來進行給予引數的方法 關鍵字引數：透過與函式的參數名稱來進行給予引數的方法

#### 實驗室 2 - 位置引數

```python
def lab_print(parameter1, parameter2):
    print(parameter1 + " and " + parameter2 + ", welecome")

argument1 = "GAIS1"
argument2 = "GAIS2"
lab_print(argument1, argument2)
```

#### 實驗室 3 - 位置引數2

```python
def lab_print(parameter1, parameter2):
    print(parameter1 + " and " + parameter2 + ", welecome")

argument1 = "GAIS1"
argument2 = "GAIS2"
lab_print(argument2, argument1)
```

可以看到我們實驗室2以及3所提供的範例，我們可以明顯感受到，當我們的引數\(呼叫函式所提供的變數`lab_print(argument2, argument1)`\)位置不一樣的時候，所印出的樣貌也不一樣。這是因為我們目前所給予函式參數的時候，所使用的位置引數方法。

#### 實驗室 4 - 關鍵字引數

有時候我們可能會因為忘記函式上的參數位置，導致引數的順序放錯了，這時候我們可以考慮使用關鍵字引數。

```python
def lab_print(parameter1, parameter2):
    print(parameter1 + " and " + parameter2 + ", welecome")

argument1 = "GAIS1"
argument2 = "GAIS2"
lab_print(parameter1=argument1, parameter2=argument2)
```

#### 實驗室 5 - 關鍵字引數

有時候我們可能會因為忘記函式上的參數位置，導致引數的順序放錯了，這時候我們可以考慮使用關鍵字引數。

```python
def lab_print(parameter1, parameter2):
    print(parameter1 + " and " + parameter2 + ", welecome")

argument1 = "GAIS1"
argument2 = "GAIS2"
lab_print(parameter2=argument2, parameter1=argument1)
```

透過實驗室4和5所提供的範例輸出，我們可以看到，輸出的結果都是一樣的。這是因為我們這次引數給予函式參數的方法是關鍵字引數。意思就是說，我們在引數\(`argument1`\)給予的時候有告訴函式，我要給的是哪個參數\(`parameter1`\)。

### 預設值

有時候，我們所定義的函式少部分時間是不需要某些參數的。這時侯我們就能夠透過先行給予參數一個預設的值，如果沒有接收到引數所傳來的資訊，那就把它當成當初設定好的預設值。

#### 實驗室 6 - 預設值

```python
def lab_print(parameter1, parameter2="GAIS2"):
    print(parameter1 + " and " + parameter2 + ", welecome")

argument1 = "GAIS1"
lab_print(parameter1=argument1)
```

#### 實驗室 7 - 預設值

```python
def lab_print(parameter1, parameter2="GAIS2"):
    print(parameter1 + " and " + parameter2 + ", welecome")

argument1 = "GAIS1"
argument3 = "GAIS3"
lab_print(parameter1=argument1, parameter2=argument3)
```

透過實驗室6和7的範例輸出，我們可以看到，在實驗室6的時候，我們沒有給予 `parameter2` 引數，卻還是印出 `GAIS2` 了，這是因為預設值的功勞。 當然如果今天我想給予不一樣的引數到函式上，在實驗室7的時候，我們給予 `parameter2` 引數為 `argument3`\(`GAIS3`\)。


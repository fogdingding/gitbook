# 函式的風格

在撰寫函式的時候，python社群有對於這件事情做一些小小的規範，主要是因為如果大家撰寫的方式能夠一樣，在於閱讀其他人程式碼的時候就能夠快速的了解其意思等好處。

### 風格

1. 函式取名的時候，需要具有描述性的名字，以及只用小寫英文字母和底線。（這可以讓未來的您以及他人快速了解這一函式在做什麼）
2. 每個函式都應該為它加入一些註解描述，讓人閱讀這一段註解就能知道這一段程式碼或是函式在做些什麼。
3. 在定義函式的時候，有時候我們需要設定預設值，這邊等號兩邊不要有空格; 當然，在用引數傳入的時候，等號兩邊也不要有空格。

#### 實驗室 1 - 函式的風格

```python
# 第一點的部分，函式名稱命名
def return_namd(first_name, middle_name='', last_name):
    # 第二點的部分，函式名稱命名
    '''
    建立一個能夠回傳外國人名以及中華人民的姓名的函式。
    '''
    if(middle_name):
        Name = first_name + ' ' + middle_name + ' ' + last_name
    else:
        Name = first_name + ' ' + last_name
    return Name


first_name = "Erich"
middle_name = "Maria"
last_name = "Remarque"

Name = return_namd(first_name, middle_name, last_name)
print(Name)


first_name = "丁白"
last_name = "張"
# 第三點的部分，等號兩邊不要有空白
Name = return_namd(first_name=first_name, last_name=last_name)
print(Name)
```

> 這件事情並沒有強制規範，換句話說就算不符合也能夠執行。但是還是希望大家能夠持有這項優良的習慣！ 下面資料來源有提供相關的更詳細的程式碼編寫規則

### 資料來源

[python-PEP8](https://www.python.org/dev/peps/pep-0008/)


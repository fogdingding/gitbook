# 彈性化的函式

今天我們要來介紹一下彈性化的函式，什麼彈性化呢？ 假設今天我們需要印出一位古老的外國人名，而這位古老的外國人名通常會有名＋中間名＋姓。以及一位古老的中華平民的姓名，這位古老的中華平民姓名為名＋姓。 意思就是說，今天我們印出的人名，有可能沒有中間名，這時候我們應該怎麼辦呢？ 別急，讓我應用之前所學的 `if ... else` 、 `預設值` 、 `關鍵字引數` 以及 `return` 來建立一個彈性化的函式吧！

#### 實驗室 1 - 彈性化的函式

首先我們先建立一個簡單的函式，能夠回傳人名字串。

```python
def return_namd(first_name, middle_name, last_name):
    Name = first_name + ' ' + middle_name + ' ' + last_name
    return Name


first_name = "Erich"
middle_name = "Maria"
last_name = "Remarque"

Name = return_namd(first_name, middle_name, last_name)
print(Name)
```

在順利建立好，能夠回人名字串後，我們將進行下一步，預設值以及決策\(`if ... else`\)的部分。

#### 實驗室 2 - 【手賤特區】彈性化的函式2

```python
def return_namd(first_name, middle_name='', last_name):
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
Name = return_namd(first_name, last_name)
print(Name)
```

這時候會跳出error，還記得嗎，當我們給予的引數跟參數順序和數量不一樣的時候，我們需要做的就是關鍵字引數方法。 因此我們再稍微修正一下。

#### 實驗室 3 - 彈性化的函式3

```python
def return_namd(first_name, middle_name='', last_name):
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
Name = return_namd(first_name=first_name, last_name=last_name)
print(Name)
```

這時候我們就能順利的輸出我們依據給予的為外國人名還是的中華人名了，來輸出不同的姓名。


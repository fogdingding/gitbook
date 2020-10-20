# 該值是否存在於串列或元組中

### 使用 `in` 檢驗是否存在該元素

我們可以藉由 `in` 這個字，來查看這個值是否存在於串列或元組中，例如：有一個使用者列表，我申請帳號時要避免使用者帳號重複，所以要先檢測是否存在於已申辦的使用者帳號中。

#### 實驗室 1 - 檢測該帳號是否存在

```python
users = ['juice', 'admin', 'may', 'john']
newUser = 'may'

if newUser in users:
  print('此帳號已申辦過，請使用別組帳號')
else:
  users.append(newUser)
```

實驗室 1 可以發現到，`newUser` 是我們要申辦的帳號，名叫 `may`，但是 `may` 這個帳號已經存在於 `users` 串列中，所以就會輸出 `此帳號已申辦過，請使用別組帳號`。

如果要檢測是否「不存在」串列中，又該怎麼做呢？

#### 實驗室 2 - 檢測該帳號是否不在黑名單中

```python
blacklist = ['attacker1', 'flush', 'shutdown', 'crash']
newUser = 'may'

if newUser not in blacklist:
  print('此帳號不在黑名單中')
else:
  print('此帳號在黑名單中')
```

使用 `not` 冠在 `in` 之前，就可以檢測該元素是否「不」存在於指定串列中。

檢測元素是否存在於元組的方式與串列相同，在此不再贅述。


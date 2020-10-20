# for、if 與串列的合併使用

這些東西我們會合在一起使用，例如今天有一串要加入會員的會員名單，我們需要一邊檢測是否與現存會員名稱衝突，一邊加入會員；這時候就會使用到 `for` 與 `if` 了：

#### 實驗室 1 - 有好大一串會員要加入公會

```python
existedMembers = ['John', 'May', 'Merry', 'Tom', 'Juice', 'Ray', 'GAIS']

appliedMembers = ['May', 'Tera', 'Giga', 'Tom', 'Henry']

for appliedMember in appliedMembers:
  if appliedMember in existedMembers:
    print(appliedMember + ' 已存在於現存會員中')
  else:
    print('歡迎 ' + appliedMember + ' 加入本公會')
    existedMembers.append(appliedMember)

print(existedMembers)
```

在實驗室 1 的時候，`for` 迴圈會將 `appliedMembers`（欲申請會員）逐一放入到 `for` 迴圈執行，每一次執行迴圈時，我們都會用 `if` 檢測該會員是否已存在於 `existedMember` （現存會員）中；如果已經存在，那麼就告知這位會員已經存在；如果不存在，那麼就將他加入到公會中。

迴圈執行完畢後，我們將 `existedMembers` 輸出，也確實這個 `for` 與 `if` 的搭配讓我們成功加上尚未加入公會的會員。


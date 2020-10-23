# 初始設定

### 設定使用者資訊

在一開始使用Git的時候，我們必須先進行設定，告知`git`我們是誰。

```bash
# 設定使用者資訊
git config --global user.name "GAIS"
git config --global user.email "GAIS@gmail.com"
```

之後我們可以來確認一下是否成功了呢

```bash
git config --list
```

如果輸出的資訊，跟我們剛剛打的一樣，那就沒問題了

### 設定編輯器

```bash
# 設定預設編輯器
git config --global core.editor "vim"
```

### 設定別名

在`git` 裡面內，有許多指令可以使用，常見的有`checkout` 、 `branch` 、 `status` ，但是有時候我們不想打那麼多字，或是常常不小心打錯字。這時候應該怎麼辦呢？

```bash
$ git config --global alias.co checkout
$ git config --global alias.br branch
$ git config --global alias.st status
```

這樣以後就可以打`git co` 來代替 `git checkout` 了




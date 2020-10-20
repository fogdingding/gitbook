# if ... elif ... else 陳述句

生活上有許多狀況，處理一件事情可能需要因應不同的狀況，有許多備案，例如：今天如果天氣冷，就吃火鍋、天氣熱，就吃剉冰、天氣涼，那就吃簡餐之類的；因應不同的狀況，我們可以使用 `elif` （else if，也就是否則如果）來達成這件事。

#### 實驗室 1 - 不同的天氣，不同的食物

```python
weather = 'cold'

if weather == 'hot':
  print('吃剉冰')
elif weather == 'cool':
  print('吃簡餐')
elif weather == 'cold':
  print('吃火鍋')
```

我們可以發現，使用 `elif` 就可以同時串起許多狀況，當 `weather = 'cold'` 的時候，唯一符合條件的就是 `elif weather == 'cold'`，也因此，就輸出 `吃火鍋`。

當然，我們也可以搭配著使用 `else`，來處理以上狀況皆不符合時的因應方式：

#### 實驗室 2 - 不同的天氣，不同的食物

```python
weather = 'warm'

if weather == 'hot':
  print('吃剉冰')
elif weather == 'cool':
  print('吃簡餐')
elif weather == 'cold':
  print('吃火鍋')
else:
  print('不知道吃啥')
```

當 `weather = 'warm'` 的時候，我們並沒有擬定好 `warm` 時，要執行哪一條指令，只好落到 `else` 的地方輸出 `不知道吃啥` 了。


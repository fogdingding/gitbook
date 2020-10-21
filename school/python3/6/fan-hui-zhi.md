# 返回值

執行完上一單元的程式碼後，我們學習到了參數和引數的使用，這一單元我們將介紹返回值，也就是當函式執行完畢後，函式將會回傳一些資訊回來。 我們將會需要一個python已經定義好的詞，叫做 `return` 它可以替我們把回傳的值順利的發送回來，相當於一個郵差。

#### 實驗室 1 - 返回值

```python
def lab_print(parameter):
    message = "Hello " + parameter
    return message

argument = "GAIS"
message_return = lab_print(argument)
print(message_return)
```

我們可以透過實驗室1，在函式中 `return` 順利的把 `Hello GAIS` 傳送回來（我們把傳送回來的值，放入變數 `message_return` 上），在進行印出，確保我們真的有接收到訊息。


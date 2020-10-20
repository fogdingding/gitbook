# 多個字典包在串列中

我們商品都需要登記價格、產地以及生產年，這三項屬性形成一個鍵值配對的字典，如果有多筆商品時，我們可以用串列將這些東西捆在一起使用：

#### 實驗室 1 - 三樣商品

```python
product_1 = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015}

product_2 = {'price' : 4000,
           'countryOfOrigin' : 'Japan',
           'manufactureYear' : 2017}

product_3 = {'price' : 500,
           'countryOfOrigin' : 'UK',
           'manufactureYear' : 2019}

products = [product_1, product_2, product_3]

print('第二項產品的價格：')
print(products[1]['price'])
```

包覆在一起時，我們就可以使用串列存取這些字典，再利用鍵去存取該字典的值。

當我們開始需要動態加入商品時，我們可以使用 `append` 方法，將新的產品字典放入到串列中：

#### 實驗室 2 - 利用 `input` 加入商品

```python
product_1 = {'price' : 135,
           'countryOfOrigin' : 'Taiwan',
           'manufactureYear' : 2015}

product_2 = {'price' : 4000,
           'countryOfOrigin' : 'Japan',
           'manufactureYear' : 2017}

product_3 = {'price' : 500,
           'countryOfOrigin' : 'UK',
           'manufactureYear' : 2019}

products = [product_1, product_2, product_3]

newProduct = {}

newProduct['price'] = int(input('請輸入商品價格：'))
newProduct['countryOfOrigin'] = input('請輸入商品產地：')
newProduct['manufactureYear'] = int(input('請輸入商品年份：'))

products.append(newProduct)

print(products)
```

如此一來，我們就可以建立一個使用者介面讓用戶自行建立新產品了。


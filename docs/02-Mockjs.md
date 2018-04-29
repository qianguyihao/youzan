
## RAP文档中的常见Mock规则

打开如下链接：<https://github.com/thx/RAP/wiki/user_manual_cn#%E5%89%8D%E7%AB%AFmock%E6%95%B0%E6%8D%AE%E7%94%9F%E6%88%90>

可以看到，RAP文档中的常见Mock规则如下：

20180429_2220.png


如果想看完整的Mock规则，可以点开 Mockjs 的官网：<http://mockjs.com/examples.html>




## RAP文档中的常见Mock规则（举例）

### 浮点数（price）

举个例子，如果我们想要给一个商品定价格（price），它的数值一般是精确到两位小数。

浮点数的规则，在mockjs上的截图如下：

20180429_2235.png

那我们在 RAP 上可以这样定义规则：

```
@mock=@float(60,100,2,2)
```

上面这行的意思是，生成一个随机数，范围在60～100之间，小数点保留两位。


我们在RAP上看一下效果：

- url：<http://rapapi.org/mockjsdata/33843/index/hotListsTest>

在浏览器上打开的效果：

20180429_2246.png

上图中，我们看到，确实按照规则，随机生成了浮点数。


### 图片的url

那图片的url，该怎么随机生成呢？它在 mockjs上的截图如下：


20180429_2252.png

那我们在 RAP 上可以这样定义规则：


```
@mock=@image('200x100', '#4A7BF7', 'Hello')
```


上面这行的三个参数，分别代表：图片的尺寸、背景色、文字。

生成的mock数据如下：(图片的url确实生成了，而且可以直接在浏览器中打开)

```json
{
    "lists": [
        {
            "img": "http://dummyimage.com/200x100/4A7BF7&text=Hello",
            "name": "测试内容pn2y",
            "price": 68.12
        },
        {
            "img": "http://dummyimage.com/200x100/4A7BF7&text=Hello",
            "name": "测试内容pn2y",
            "price": 92.55
        },
        {
            "img": "http://dummyimage.com/200x100/4A7BF7&text=Hello",
            "name": "测试内容pn2y",
            "price": 83.68
        },
        {
            "img": "http://dummyimage.com/200x100/4A7BF7&text=Hello",
            "name": "测试内容pn2y",
            "price": 75.59
        }
    ]
}
```


上面的json数据中，我们发现，图片的背景色都是一样的，那如果我想随机生成背景色，该怎么做呢？

很简单，











上图中的规则指的是：

> 











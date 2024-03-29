## 文档结构

* DOCTYPE ：
DOCTYPE是document type(文档类型)的简写，用来声明文档类型，告诉浏览器的文档解释器，用什么方式解释文档，包括
1. 告诉浏览器要处理的是html文档；
2. 标记文档内容的版本
3. 浏览器根据DOCTYPE决定使用哪种渲染模式
4. 必须位于html文档第一行，不是html标签

* 渲染模式：
1. 怪异模式
2. 准标准模式
3. 标准模式
    如果网页代码不含有任何声明，那么浏览器就会采用怪异模式解析，
    如果你的网页代码含有DTD声明，浏览器就会按你所声明的标准解析

* 文档结构标签
  html、head、title、meta、link、script、body

```
<!DOCTYPE HTML>
<html>
<head>
    <title>Example</title>
    <base href="http://titan/listings/"/>
    <meta name="author" content="Adam Freeman"/>
    <meta name="description" content="A simple example"/>
    <meta charset="utf-8"/>
    <link href="theme.css" rel="stylesheet" type="text/css">
    <script src="1.js" type="text/javascript" ></script>
</head>
<body>
<p>
    I like apples and oranges.
</p>
</body>
</html>
```


```
<base href="http://www.w3school.com.cn/css/" target="_blank" />
</head>

<body>
<a href="index.asp">W3School's CSS Tutorial</a>
</body>
```



文档编码

```
<meta charset="utf-8"/>
```


页面小图标

```
<head>
    <meta charset="UTF-8">
    <!--页面小图标-->
    <link rel="icon" href="./mooc_icon.png">
    <title>Title</title>
</head>
```

设置referer
如请求其他服务器（百度）上的图片

```
<meta name="referer" content ="never" >
```

页面描述

```
<meta name="description" content="A simple example"/>
```

适配移动端页面

```
<meta name="viewport" content="width=device-width,initial-sacle=1.0"/>
```

定制页面图标

```
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
```


## meta 常见值：
1、name属性：可取的值为 keywords(关键字)；  description(网站内容的描述)； viewport(移动端的窗口)；author(作者) 等等；
2、http-equiv属性 ：可取的值包括  content-Type(设定网页字符集) ；cache-control(指定请求和响应遵循的缓存机制)；. expires(网页到期时间)； refresh(自动刷新并指向某页面)

- charset	character      encoding 定义文档的字符编码。	   
- content	some_text	   定义与 http-equiv 或 name 属性相关的元信息。  
- http-equiv	 把 content 属性关联到 HTTP 头部。   
  content-type   
  expires   
  refresh   
  set-cookie   

- name	 把 content 属性关联到一个名称。
  author
  description
  keywords
  generator
  revised
  others
 
## 乱码问题
- 英文和数字不会出现乱码，中文可能会出现
- 给 HTML 的 head 标签里加 <meta charset="utf-8"> 不一定能解决乱码问题
- 页面保存的时候用的是什么编码格式，就给 HTML 的 head 标签里meta 的 charset 属性设置相同编码格式
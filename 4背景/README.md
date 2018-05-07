# 背景

## 背景颜色background-color
* 可简写为background
* 默认值为transparent
* 可取属性值，color_name、transparent、inherit
### 示例
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        p{
            height: 40px;
            width:600px;
            background-color: blueviolet;
            color: white;
            text-align: center; /*文字居中*/
            line-height:40px; /*行高与width一致，保证文字上下居中*/
            margin:60px auto;/*块居中*/
        }
    </style>
</head>
<body>
    <p >This is a test paragraph</p>
</body>
</html>
```

### 效果
 ![背景颜色](./bgcolor.png)

## 背景图片background-img
* url 图片的url
* 默认值为none
* 可取属性值，url、none、inherit
### 示例
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .logo a{
            background-image: url(http://www.baidu.com/img/baidu_jgylogo3.gif);
            display: block; /*a标签默认行内元素，设置宽、高不起作用*/
            height: 38px;
            width: 117px;
            text-indent: -9999px;
        }
    </style>
</head>
<body>
    <h1 class="logo">
        <a href="#">baidu</a>
    </h1>
</body>
</html>
```

### 效果
 ![背景图片](./bgimg.png)

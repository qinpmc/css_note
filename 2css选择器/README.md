# css 选择器

## css基本选择器

* 标签选择器，如：div{ color:red; }
* 类选择器 ,如：.class1{color:yellow;}
* Id选择器，如 #id1{ color:blue;}
* 通配符选择器 *
* 属性选择器，如[href]{ border:thin solid black}

## 属性选择器

* ![属性选择器](./attrselector.png)

### 示例
```
<!DOCTYPE html>
<html >
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        *{

        }
        [class~="class2"] {
            border: thin red solid;
            padding: 4px;
        }
        [lang|="en"] {
            border: thick blue dashed;
            padding: 4px;
        }
    </style>
</head>
<body>
    <a id="apressanchor" class="class1 class2" href="http://apress.com">
        Visit the Apress website
    </a>
    <p>I like <span class="class2">apples</span> and oranges.</p>
    <hr>
    <a lang="en-us"   href="http://apress.com">
        Visit the Bpress website
    </a>
    <p>I like <span lang="en-gb"  >apples</span> and oranges.</p>
    <a lang="en"  href="http://w3c.org">Visit the W3C website</a>
</body>
</html>
```
### 效果
* ![属性选择器效果](./res1.png)


## 复合选择器
* 并集选择器，如a,p{ color:red;}
* 后代选择器，如p span{ color:red;},包含p中任意的span，不仅仅是子元素
* 子选择器，如 p>span{ color:red;}
* 相邻兄弟选择器，如p+span{ color:red;}
* 普通兄弟选择器，如p~span{ color:red;}，包含所有的兄弟，不仅仅是相邻的，只包括p后面的兄弟元素，不包含p前面的兄弟

## 伪类选择器
### 动态伪类选择器
* :linked
* :visited
* :hover
* :active
* :focus

### 否定选择器
* :not，css3

### 伪元素选择器
* ::first-line
* ::first-letter
* :before :after ,会生成内容，如 a:before{content:"click here" }

### 结构性伪类选择器
* :first-child
* :last-child ，css3
* :only-child ,匹配父元素包含的唯一子元素，css3
* :only-of-type
* :nth-child(n),父元素的第n个子元素，css3
* :nth-last-child(n),父元素的倒数第n个子元素，css3

### UI伪类选择器
* :enabled
* :disabled
* :checked
* :valid
* :invalid
* :rquired
* :default
* :in-range
* :out-of-range
* :optional



### 示例
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style type="text/css">
        a{
            text-decoration: none;
        }
        a:link{color:red}
        a:hover{text-decoration:underline}
        a:active{background: yellow}
        a:visited{color:grey}

        li{
            border:solid 2px red
        }
        li:not(:last-child){
            border:solid 2px blue
        }
    </style>
</head>
<body>
<a href="http://www.sina.com">跳转去百度</a>
<ul>
    <li>li1</li>
    <li>li2</li>
    <li>li3</li>
</ul>
</body>
</html>
```

### 效果
* ![伪类选择器效果](./res2.png)



